---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 84e2942037ba0d01425ca85530d33a042544dafc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992472"
---
# <span data-ttu-id="ad46d-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="ad46d-101">Get-AzADGroup</span></span>

## <span data-ttu-id="ad46d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad46d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad46d-103">Filtra i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad46d-103">Filters active directory groups.</span></span>

## <span data-ttu-id="ad46d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad46d-104">SYNTAX</span></span>

### <span data-ttu-id="ad46d-105">EmptyParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad46d-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ad46d-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad46d-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ad46d-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad46d-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="ad46d-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad46d-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="ad46d-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad46d-109">DESCRIPTION</span></span>
<span data-ttu-id="ad46d-110">Filtra i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ad46d-110">Filters active directory groups.</span></span>

## <span data-ttu-id="ad46d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad46d-111">EXAMPLES</span></span>

### <span data-ttu-id="ad46d-112">Esempio 1: Elencare tutti i gruppi di Active Directory</span><span class="sxs-lookup"><span data-stu-id="ad46d-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="ad46d-113">Elenca tutti i gruppi di Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="ad46d-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="ad46d-114">Esempio 2: Elencare tutti i gruppi di Active Directory tramite la suddivisione in pagine</span><span class="sxs-lookup"><span data-stu-id="ad46d-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="ad46d-115">Elenca i primi 100 gruppi di Active Directory in un tenant.</span><span class="sxs-lookup"><span data-stu-id="ad46d-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="ad46d-116">Esempio 3: Ottenere Active Directory Group per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="ad46d-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="ad46d-117">Ottiene un gruppo Active Directory con ID oggetto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="ad46d-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="ad46d-118">Esempio 4: Elencare gruppi per stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="ad46d-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="ad46d-119">Elenca tutti i gruppi di Active Directory il cui nome visualizzato inizia con "Luca".</span><span class="sxs-lookup"><span data-stu-id="ad46d-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="ad46d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad46d-120">PARAMETERS</span></span>

### <span data-ttu-id="ad46d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad46d-121">-DefaultProfile</span></span>
<span data-ttu-id="ad46d-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ad46d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad46d-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ad46d-123">-DisplayName</span></span>
<span data-ttu-id="ad46d-124">Nome visualizzato del gruppo.</span><span class="sxs-lookup"><span data-stu-id="ad46d-124">The display name of the group.</span></span>

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

### <span data-ttu-id="ad46d-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="ad46d-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="ad46d-126">Consente di trovare gruppi che iniziano con la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="ad46d-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="ad46d-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ad46d-127">-ObjectId</span></span>
<span data-ttu-id="ad46d-128">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="ad46d-128">Object id of the group.</span></span>

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

### <span data-ttu-id="ad46d-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="ad46d-129">-IncludeTotalCount</span></span>
<span data-ttu-id="ad46d-130">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="ad46d-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="ad46d-131">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="ad46d-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="ad46d-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="ad46d-132">-Skip</span></span>
<span data-ttu-id="ad46d-133">Ignora i primi N oggetti e quindi ottiene gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="ad46d-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="ad46d-134">-First</span><span class="sxs-lookup"><span data-stu-id="ad46d-134">-First</span></span>
<span data-ttu-id="ad46d-135">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="ad46d-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="ad46d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad46d-136">CommonParameters</span></span>
<span data-ttu-id="ad46d-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad46d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad46d-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad46d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad46d-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad46d-139">INPUTS</span></span>

### <span data-ttu-id="ad46d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ad46d-140">System.String</span></span>

### <span data-ttu-id="ad46d-141">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ad46d-141">System.Guid</span></span>

## <span data-ttu-id="ad46d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad46d-142">OUTPUTS</span></span>

### <span data-ttu-id="ad46d-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="ad46d-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="ad46d-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad46d-144">NOTES</span></span>

## <span data-ttu-id="ad46d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad46d-145">RELATED LINKS</span></span>

[<span data-ttu-id="ad46d-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ad46d-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="ad46d-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ad46d-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="ad46d-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="ad46d-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

