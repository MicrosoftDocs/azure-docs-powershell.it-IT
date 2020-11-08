---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 764b2d091b0019cc4231828066b4067c5f054476
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188948"
---
# <span data-ttu-id="28dbc-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="28dbc-101">Get-AzADGroup</span></span>

## <span data-ttu-id="28dbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="28dbc-103">Filtra i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="28dbc-103">Filters active directory groups.</span></span>

## <span data-ttu-id="28dbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28dbc-104">SYNTAX</span></span>

### <span data-ttu-id="28dbc-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28dbc-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="28dbc-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="28dbc-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="28dbc-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="28dbc-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="28dbc-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28dbc-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="28dbc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28dbc-109">DESCRIPTION</span></span>
<span data-ttu-id="28dbc-110">Filtra i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="28dbc-110">Filters active directory groups.</span></span>

## <span data-ttu-id="28dbc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28dbc-111">EXAMPLES</span></span>

### <span data-ttu-id="28dbc-112">Esempio 1: elenca tutti i gruppi di annunci</span><span class="sxs-lookup"><span data-stu-id="28dbc-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="28dbc-113">Elenca tutti i gruppi di annunci in un tenant.</span><span class="sxs-lookup"><span data-stu-id="28dbc-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="28dbc-114">Esempio 2: elencare tutti i gruppi di annunci tramite paging</span><span class="sxs-lookup"><span data-stu-id="28dbc-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="28dbc-115">Elenca i primi gruppi di annunci di 100 in un tenant.</span><span class="sxs-lookup"><span data-stu-id="28dbc-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="28dbc-116">Esempio 3: ottenere un gruppo di annunci per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="28dbc-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="28dbc-117">Ottiene un gruppo di annunci con ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="28dbc-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="28dbc-118">Esempio 4: gruppi di elenco per stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="28dbc-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="28dbc-119">Elenca tutti i gruppi di annunci il cui nome visualizzato inizia con "Joe".</span><span class="sxs-lookup"><span data-stu-id="28dbc-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="28dbc-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28dbc-120">PARAMETERS</span></span>

### <span data-ttu-id="28dbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28dbc-121">-DefaultProfile</span></span>
<span data-ttu-id="28dbc-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="28dbc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbc-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="28dbc-123">-DisplayName</span></span>
<span data-ttu-id="28dbc-124">Il nome visualizzato del gruppo.</span><span class="sxs-lookup"><span data-stu-id="28dbc-124">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbc-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="28dbc-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="28dbc-126">Usato per trovare i gruppi che iniziano con la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="28dbc-126">Used to find groups that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28dbc-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="28dbc-127">-ObjectId</span></span>
<span data-ttu-id="28dbc-128">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="28dbc-128">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28dbc-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="28dbc-129">-IncludeTotalCount</span></span>
<span data-ttu-id="28dbc-130">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="28dbc-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="28dbc-131">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="28dbc-131">Currently, this parameter does nothing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbc-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="28dbc-132">-Skip</span></span>
<span data-ttu-id="28dbc-133">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="28dbc-133">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbc-134">-Primo</span><span class="sxs-lookup"><span data-stu-id="28dbc-134">-First</span></span>
<span data-ttu-id="28dbc-135">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="28dbc-135">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28dbc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28dbc-136">CommonParameters</span></span>
<span data-ttu-id="28dbc-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28dbc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28dbc-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28dbc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28dbc-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28dbc-139">INPUTS</span></span>

### <span data-ttu-id="28dbc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="28dbc-140">System.String</span></span>

### <span data-ttu-id="28dbc-141">System. Guid</span><span class="sxs-lookup"><span data-stu-id="28dbc-141">System.Guid</span></span>

## <span data-ttu-id="28dbc-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28dbc-142">OUTPUTS</span></span>

### <span data-ttu-id="28dbc-143">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="28dbc-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="28dbc-144">Note</span><span class="sxs-lookup"><span data-stu-id="28dbc-144">NOTES</span></span>

## <span data-ttu-id="28dbc-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28dbc-145">RELATED LINKS</span></span>

[<span data-ttu-id="28dbc-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="28dbc-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="28dbc-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="28dbc-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="28dbc-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="28dbc-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

