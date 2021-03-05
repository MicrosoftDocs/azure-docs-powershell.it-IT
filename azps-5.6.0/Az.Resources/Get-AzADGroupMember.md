---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: d351ee85c36b9f5f8493879cded058fd7220450f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986676"
---
# <span data-ttu-id="fa140-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="fa140-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="fa140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa140-102">SYNOPSIS</span></span>
<span data-ttu-id="fa140-103">Elenca i membri di un gruppo active directory nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="fa140-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="fa140-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa140-104">SYNTAX</span></span>

### <span data-ttu-id="fa140-105">ObjectIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa140-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fa140-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa140-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="fa140-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa140-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="fa140-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fa140-108">DESCRIPTION</span></span>
<span data-ttu-id="fa140-109">Elenca i membri di un gruppo active directory nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="fa140-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="fa140-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa140-110">EXAMPLES</span></span>

### <span data-ttu-id="fa140-111">Esempio 1: Elencare i membri in base all'ID oggetto gruppo Di Active Directory</span><span class="sxs-lookup"><span data-stu-id="fa140-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="fa140-112">Elenca i membri del gruppo Active Directory con ID oggetto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="fa140-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="fa140-113">Esempio 2: Elencare i membri in base all'ID oggetto gruppo di Active Directory usando il paging</span><span class="sxs-lookup"><span data-stu-id="fa140-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="fa140-114">Elenca i primi 100 membri del gruppo Active Directory con ID oggetto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="fa140-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="fa140-115">Esempio 3: Elencare i membri tramite piping</span><span class="sxs-lookup"><span data-stu-id="fa140-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="fa140-116">Ottiene il gruppo Active Directory con ID oggetto '85F89C90-780E-4AA6-9F4F-6F268D322EEE' e lo pipe al cmdlet di Get-AzADGroupMember per elencare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="fa140-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="fa140-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa140-117">PARAMETERS</span></span>

### <span data-ttu-id="fa140-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa140-118">-DefaultProfile</span></span>
<span data-ttu-id="fa140-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fa140-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa140-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="fa140-120">-GroupDisplayName</span></span>
<span data-ttu-id="fa140-121">Nome visualizzato del gruppo.</span><span class="sxs-lookup"><span data-stu-id="fa140-121">The display name of the group.</span></span>

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

### <span data-ttu-id="fa140-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="fa140-122">-GroupObject</span></span>
<span data-ttu-id="fa140-123">Oggetto gruppo da cui si stanno elencando i membri.</span><span class="sxs-lookup"><span data-stu-id="fa140-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa140-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="fa140-124">-GroupObjectId</span></span>
<span data-ttu-id="fa140-125">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="fa140-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa140-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="fa140-126">-IncludeTotalCount</span></span>
<span data-ttu-id="fa140-127">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="fa140-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="fa140-128">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="fa140-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="fa140-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="fa140-129">-Skip</span></span>
<span data-ttu-id="fa140-130">Ignora i primi N oggetti e quindi ottiene gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="fa140-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="fa140-131">-First</span><span class="sxs-lookup"><span data-stu-id="fa140-131">-First</span></span>
<span data-ttu-id="fa140-132">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="fa140-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="fa140-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa140-133">CommonParameters</span></span>
<span data-ttu-id="fa140-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa140-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa140-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fa140-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa140-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="fa140-136">INPUTS</span></span>

### <span data-ttu-id="fa140-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fa140-137">System.String</span></span>

### <span data-ttu-id="fa140-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="fa140-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="fa140-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa140-139">OUTPUTS</span></span>

### <span data-ttu-id="fa140-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span><span class="sxs-lookup"><span data-stu-id="fa140-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="fa140-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="fa140-141">NOTES</span></span>

## <span data-ttu-id="fa140-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa140-142">RELATED LINKS</span></span>

[<span data-ttu-id="fa140-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="fa140-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="fa140-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="fa140-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

