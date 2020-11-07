---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 25de035b853d1a17ee06a7efb6ac31631bd466f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677411"
---
# <span data-ttu-id="5d9ff-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="5d9ff-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="5d9ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="5d9ff-103">Elenca i membri di un gruppo di annunci nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="5d9ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d9ff-104">SYNTAX</span></span>

### <span data-ttu-id="5d9ff-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d9ff-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5d9ff-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d9ff-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5d9ff-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d9ff-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="5d9ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d9ff-108">DESCRIPTION</span></span>
<span data-ttu-id="5d9ff-109">Elenca i membri di un gruppo di annunci nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="5d9ff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d9ff-110">EXAMPLES</span></span>

### <span data-ttu-id="5d9ff-111">Esempio 1-elenca i membri per ID oggetto gruppo AD</span><span class="sxs-lookup"><span data-stu-id="5d9ff-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="5d9ff-112">Elenca i membri del gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="5d9ff-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5d9ff-113">Esempio 2-elenca i membri per ID oggetto gruppo di annunci tramite paging</span><span class="sxs-lookup"><span data-stu-id="5d9ff-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="5d9ff-114">Elenca i primi 100 membri del gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="5d9ff-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5d9ff-115">Esempio 3-elenca i membri per piping</span><span class="sxs-lookup"><span data-stu-id="5d9ff-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="5d9ff-116">Ottiene il gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" e lo convoglia al cmdlet Get-AzADGroupMember per elencare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="5d9ff-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d9ff-117">PARAMETERS</span></span>

### <span data-ttu-id="5d9ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d9ff-118">-DefaultProfile</span></span>
<span data-ttu-id="5d9ff-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5d9ff-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d9ff-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="5d9ff-120">-GroupDisplayName</span></span>
<span data-ttu-id="5d9ff-121">Il nome visualizzato del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-121">The display name of the group.</span></span>

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

### <span data-ttu-id="5d9ff-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="5d9ff-122">-GroupObject</span></span>
<span data-ttu-id="5d9ff-123">Oggetto Group di cui si stanno elencando i membri.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-123">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="5d9ff-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="5d9ff-124">-GroupObjectId</span></span>
<span data-ttu-id="5d9ff-125">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-125">Object Id of the group.</span></span>

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

### <span data-ttu-id="5d9ff-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="5d9ff-126">-IncludeTotalCount</span></span>
<span data-ttu-id="5d9ff-127">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="5d9ff-128">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="5d9ff-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="5d9ff-129">-Skip</span></span>
<span data-ttu-id="5d9ff-130">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="5d9ff-131">-Primo</span><span class="sxs-lookup"><span data-stu-id="5d9ff-131">-First</span></span>
<span data-ttu-id="5d9ff-132">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="5d9ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d9ff-133">CommonParameters</span></span>
<span data-ttu-id="5d9ff-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d9ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d9ff-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d9ff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d9ff-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d9ff-136">INPUTS</span></span>

### <span data-ttu-id="5d9ff-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5d9ff-137">System.String</span></span>

### <span data-ttu-id="5d9ff-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5d9ff-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="5d9ff-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d9ff-139">OUTPUTS</span></span>

### <span data-ttu-id="5d9ff-140">Microsoft. Azure. Commands. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="5d9ff-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="5d9ff-141">Note</span><span class="sxs-lookup"><span data-stu-id="5d9ff-141">NOTES</span></span>

## <span data-ttu-id="5d9ff-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d9ff-142">RELATED LINKS</span></span>

[<span data-ttu-id="5d9ff-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5d9ff-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="5d9ff-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d9ff-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

