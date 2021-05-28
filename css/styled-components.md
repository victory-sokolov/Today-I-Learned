# Styled Components

### Extend style


```javascript
const Grid = styled.div`
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  justify-content: center;
`
```


```javascript
const GridExtended = styled(Grid)`
    grid-gap: 32px;
    margin-top: 40px;
    padding-bottom: 45px;
`;
```
