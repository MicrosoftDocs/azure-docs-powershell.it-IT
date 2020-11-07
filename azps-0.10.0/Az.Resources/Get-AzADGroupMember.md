---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: f083498860f3f2b9e19280b41d953032796e0eb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862633"
---
# <span data-ttu-id="7b065-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="7b065-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="7b065-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b065-102">SYNOPSIS</span></span>
<span data-ttu-id="7b065-103">Elenca i membri di un gruppo di annunci nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="7b065-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="7b065-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b065-104">SYNTAX</span></span>

### <span data-ttu-id="7b065-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b065-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7b065-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b065-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="7b065-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b065-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="7b065-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b065-108">DESCRIPTION</span></span>
<span data-ttu-id="7b065-109">Elenca i membri di un gruppo di annunci nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="7b065-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="7b065-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b065-110">EXAMPLES</span></span>

### <span data-ttu-id="7b065-111">Esempio 1-elenca i membri per ID oggetto gruppo AD</span><span class="sxs-lookup"><span data-stu-id="7b065-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="7b065-112">Elenca i membri del gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="7b065-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="7b065-113">Esempio 2-elenca i membri per ID oggetto gruppo di annunci tramite paging</span><span class="sxs-lookup"><span data-stu-id="7b065-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="7b065-114">Elenca i primi 100 membri del gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="7b065-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="7b065-115">Esempio 3-elenca i membri per piping</span><span class="sxs-lookup"><span data-stu-id="7b065-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="7b065-116">Ottiene il gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" e lo convoglia al cmdlet Get-AzADGroupMember per elencare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="7b065-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="7b065-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b065-117">PARAMETERS</span></span>

### <span data-ttu-id="7b065-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b065-118">-DefaultProfile</span></span>
<span data-ttu-id="7b065-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7b065-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b065-120">-Primo</span><span class="sxs-lookup"><span data-stu-id="7b065-120">-First</span></span>
<span data-ttu-id="7b065-121">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="7b065-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="7b065-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="7b065-122">-GroupDisplayName</span></span>
<span data-ttu-id="7b065-123">Il nome visualizzato del gruppo.</span><span class="sxs-lookup"><span data-stu-id="7b065-123">The display name of the group.</span></span>

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

### <span data-ttu-id="7b065-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="7b065-124">-GroupObject</span></span>
<span data-ttu-id="7b065-125">Oggetto Group di cui si stanno elencando i membri.</span><span class="sxs-lookup"><span data-stu-id="7b065-125">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b065-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="7b065-126">-GroupObjectId</span></span>
<span data-ttu-id="7b065-127">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="7b065-127">Object Id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b065-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="7b065-128">-IncludeTotalCount</span></span>
<span data-ttu-id="7b065-129">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="7b065-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="7b065-130">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="7b065-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="7b065-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="7b065-131">-Skip</span></span>
<span data-ttu-id="7b065-132">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="7b065-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="7b065-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b065-133">CommonParameters</span></span>
<span data-ttu-id="7b065-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b065-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b065-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b065-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b065-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b065-136">INPUTS</span></span>

### <span data-ttu-id="7b065-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7b065-137">System.Guid</span></span>

### <span data-ttu-id="7b065-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="7b065-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="7b065-139">Parametri: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b065-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="7b065-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b065-140">OUTPUTS</span></span>

### <span data-ttu-id="7b065-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="7b065-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="7b065-142">Note</span><span class="sxs-lookup"><span data-stu-id="7b065-142">NOTES</span></span>

## <span data-ttu-id="7b065-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b065-143">RELATED LINKS</span></span>

[<span data-ttu-id="7b065-144">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="7b065-144">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="7b065-145">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7b065-145">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

