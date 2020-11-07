---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
ms.openlocfilehash: f790266f1e61446cb9d1c257929cf8b6e3ab25d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866209"
---
# <span data-ttu-id="5dc47-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="5dc47-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="5dc47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5dc47-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc47-103">Elenca i membri di un gruppo di annunci nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="5dc47-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dc47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5dc47-104">SYNTAX</span></span>

### <span data-ttu-id="5dc47-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5dc47-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5dc47-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dc47-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5dc47-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5dc47-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="5dc47-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dc47-108">DESCRIPTION</span></span>
<span data-ttu-id="5dc47-109">Elenca i membri di un gruppo di annunci nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="5dc47-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="5dc47-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5dc47-110">EXAMPLES</span></span>

### <span data-ttu-id="5dc47-111">Esempio 1-elenca i membri per ID oggetto gruppo AD</span><span class="sxs-lookup"><span data-stu-id="5dc47-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="5dc47-112">Elenca i membri del gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="5dc47-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5dc47-113">Esempio 2-elenca i membri per ID oggetto gruppo di annunci tramite paging</span><span class="sxs-lookup"><span data-stu-id="5dc47-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="5dc47-114">Elenca i primi 100 membri del gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="5dc47-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5dc47-115">Esempio 3-elenca i membri per piping</span><span class="sxs-lookup"><span data-stu-id="5dc47-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="5dc47-116">Ottiene il gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" e lo convoglia al cmdlet Get-AzureRmADGroupMember per elencare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5dc47-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="5dc47-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5dc47-117">PARAMETERS</span></span>

### <span data-ttu-id="5dc47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc47-118">-DefaultProfile</span></span>
<span data-ttu-id="5dc47-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5dc47-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dc47-120">-Primo</span><span class="sxs-lookup"><span data-stu-id="5dc47-120">-First</span></span>
<span data-ttu-id="5dc47-121">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="5dc47-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="5dc47-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="5dc47-122">-GroupDisplayName</span></span>
<span data-ttu-id="5dc47-123">Il nome visualizzato del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5dc47-123">The display name of the group.</span></span>

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

### <span data-ttu-id="5dc47-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="5dc47-124">-GroupObject</span></span>
<span data-ttu-id="5dc47-125">Oggetto Group di cui si stanno elencando i membri.</span><span class="sxs-lookup"><span data-stu-id="5dc47-125">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="5dc47-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="5dc47-126">-GroupObjectId</span></span>
<span data-ttu-id="5dc47-127">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="5dc47-127">Object Id of the group.</span></span>

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

### <span data-ttu-id="5dc47-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="5dc47-128">-IncludeTotalCount</span></span>
<span data-ttu-id="5dc47-129">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="5dc47-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="5dc47-130">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="5dc47-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="5dc47-131">-Skip</span><span class="sxs-lookup"><span data-stu-id="5dc47-131">-Skip</span></span>
<span data-ttu-id="5dc47-132">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="5dc47-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="5dc47-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc47-133">CommonParameters</span></span>
<span data-ttu-id="5dc47-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dc47-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc47-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dc47-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc47-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5dc47-136">INPUTS</span></span>

### <span data-ttu-id="5dc47-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="5dc47-137">System.Guid</span></span>

### <span data-ttu-id="5dc47-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5dc47-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="5dc47-139">Parametri: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5dc47-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="5dc47-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5dc47-140">OUTPUTS</span></span>

### <span data-ttu-id="5dc47-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="5dc47-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="5dc47-142">Note</span><span class="sxs-lookup"><span data-stu-id="5dc47-142">NOTES</span></span>

## <span data-ttu-id="5dc47-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5dc47-143">RELATED LINKS</span></span>

[<span data-ttu-id="5dc47-144">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5dc47-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="5dc47-145">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5dc47-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

