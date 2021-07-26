# JPA

{% embed url="https://velog.io/@adam2/JPA%EB%8A%94-%EB%8F%84%EB%8D%B0%EC%B2%B4-%EB%AD%98%EA%B9%8C-orm-%EC%98%81%EC%86%8D%EC%84%B1-hibernate-spring-data-jpa" %}



<table>
  <thead>
    <tr>
      <th style="text-align:left">Keyword</th>
      <th style="text-align:left">Sample</th>
      <th style="text-align:left">JPQL snippet</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><code>And</code>
      </td>
      <td style="text-align:left"><code>findByLastnameAndFirstname</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.lastname = ?1 and x.firstname = ?2</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>Or</code>
      </td>
      <td style="text-align:left"><code>findByLastnameOrFirstname</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.lastname = ?1 or x.firstname = ?2</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>Is,Equals</code>
      </td>
      <td style="text-align:left">
        <p><code>findByFirstname,</code>
        </p>
        <p><code>findByFirstnameIs,</code>
        </p>
        <p><code>findByFirstnameEquals</code>
        </p>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.firstname = 1?</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>Between</code>
      </td>
      <td style="text-align:left"><code>findByStartDateBetween</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.startDate between 1? and ?2</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>LessThan</code>
      </td>
      <td style="text-align:left"><code>findByAgeLessThan</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.age &lt; ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>LessThanEqual</code>
      </td>
      <td style="text-align:left"><code>findByAgeLessThanEqual</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.age &lt;= ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>GreaterThan</code>
      </td>
      <td style="text-align:left"><code>findByAgeGreaterThan</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.age &gt; ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>GreaterThanEqual</code>
      </td>
      <td style="text-align:left"><code>findByAgeGreaterThanEqual</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.age &gt;= ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>After</code>
      </td>
      <td style="text-align:left"><code>findByStartDateAfter</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.startDate &gt; ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>Before</code>
      </td>
      <td style="text-align:left"><code>findByStartDateBefore</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.startDate &lt; ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>IsNull</code>
      </td>
      <td style="text-align:left"><code>findByAgeIsNull</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.age is null</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>IsNotNull,NotNull</code>
      </td>
      <td style="text-align:left"><code>findByAge(Is)NotNull</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.age not null</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>Like</code>
      </td>
      <td style="text-align:left"><code>findByFirstnameLike</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.firstname like ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>NotLike</code>
      </td>
      <td style="text-align:left"><code>findByFirstnameNotLike</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.firstname not like ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>StartingWith</code>
      </td>
      <td style="text-align:left"><code>findByFirstnameStartingWith</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.firstname like ?1</code> (parameter bound with appended <code>%</code>)</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>EndingWith</code>
      </td>
      <td style="text-align:left"><code>findByFirstnameEndingWith</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.firstname like ?1</code> (parameter bound with prepended <code>%</code>)</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>Containing</code>
      </td>
      <td style="text-align:left"><code>findByFirstnameContaining</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.firstname like ?1</code> (parameter bound wrapped
        in <code>%</code>)</td>
    </tr>
    <tr>
      <td style="text-align:left"><code>OrderBy</code>
      </td>
      <td style="text-align:left"><code>findByAgeOrderByLastnameDesc</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.age = ?1 order by x.lastname desc</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>Not</code>
      </td>
      <td style="text-align:left"><code>findByLastnameNot</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.lastname &lt;&gt; ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>In</code>
      </td>
      <td style="text-align:left"><code>findByAgeIn(Collection&lt;Age&gt; ages)</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.age in ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>NotIn</code>
      </td>
      <td style="text-align:left"><code>findByAgeNotIn(Collection&lt;Age&gt; age)</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.age not in ?1</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>True</code>
      </td>
      <td style="text-align:left"><code>findByActiveTrue()</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.active = true</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>False</code>
      </td>
      <td style="text-align:left"><code>findByActiveFalse()</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where x.active = false</code>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><code>IgnoreCase</code>
      </td>
      <td style="text-align:left"><code>findByFirstnameIgnoreCase</code>
      </td>
      <td style="text-align:left"><code>&#x2026; where UPPER(x.firstame) = UPPER(?1)</code>
      </td>
    </tr>
  </tbody>
</table>



