---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 984b5ef9a1ff19142ef044e1f3c919f8fb2a3dce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366026"
---
# <span data-ttu-id="f87ef-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="f87ef-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="f87ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f87ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f87ef-103">Elenca i membri di un gruppo di annunci nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="f87ef-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="f87ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f87ef-104">SYNTAX</span></span>

### <span data-ttu-id="f87ef-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f87ef-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f87ef-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f87ef-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="f87ef-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f87ef-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="f87ef-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f87ef-108">DESCRIPTION</span></span>
<span data-ttu-id="f87ef-109">Elenca i membri di un gruppo di annunci nel tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="f87ef-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="f87ef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f87ef-110">EXAMPLES</span></span>

### <span data-ttu-id="f87ef-111">Esempio 1: elencare i membri per ID oggetto gruppo AD</span><span class="sxs-lookup"><span data-stu-id="f87ef-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="f87ef-112">Elenca i membri del gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="f87ef-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="f87ef-113">Esempio 2: elencare i membri per ID oggetto gruppo di annunci tramite paging</span><span class="sxs-lookup"><span data-stu-id="f87ef-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="f87ef-114">Elenca i primi 100 membri del gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="f87ef-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="f87ef-115">Esempio 3: elencare i membri per piping</span><span class="sxs-lookup"><span data-stu-id="f87ef-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="f87ef-116">Ottiene il gruppo di annunci con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" e lo convoglia al cmdlet Get-AzADGroupMember per elencare tutti i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f87ef-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="f87ef-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f87ef-117">PARAMETERS</span></span>

### <span data-ttu-id="f87ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87ef-118">-DefaultProfile</span></span>
<span data-ttu-id="f87ef-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f87ef-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f87ef-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="f87ef-120">-GroupDisplayName</span></span>
<span data-ttu-id="f87ef-121">Il nome visualizzato del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f87ef-121">The display name of the group.</span></span>

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

### <span data-ttu-id="f87ef-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="f87ef-122">-GroupObject</span></span>
<span data-ttu-id="f87ef-123">Oggetto Group di cui si stanno elencando i membri.</span><span class="sxs-lookup"><span data-stu-id="f87ef-123">The group object that you are listing members from.</span></span>

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

### <span data-ttu-id="f87ef-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="f87ef-124">-GroupObjectId</span></span>
<span data-ttu-id="f87ef-125">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f87ef-125">Object Id of the group.</span></span>

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

### <span data-ttu-id="f87ef-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="f87ef-126">-IncludeTotalCount</span></span>
<span data-ttu-id="f87ef-127">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="f87ef-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="f87ef-128">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="f87ef-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="f87ef-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="f87ef-129">-Skip</span></span>
<span data-ttu-id="f87ef-130">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="f87ef-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="f87ef-131">-Primo</span><span class="sxs-lookup"><span data-stu-id="f87ef-131">-First</span></span>
<span data-ttu-id="f87ef-132">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="f87ef-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="f87ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87ef-133">CommonParameters</span></span>
<span data-ttu-id="f87ef-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87ef-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f87ef-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87ef-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f87ef-136">INPUTS</span></span>

### <span data-ttu-id="f87ef-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f87ef-137">System.String</span></span>

### <span data-ttu-id="f87ef-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="f87ef-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="f87ef-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f87ef-139">OUTPUTS</span></span>

### <span data-ttu-id="f87ef-140">Microsoft. Azure. Commands. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="f87ef-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="f87ef-141">Note</span><span class="sxs-lookup"><span data-stu-id="f87ef-141">NOTES</span></span>

## <span data-ttu-id="f87ef-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f87ef-142">RELATED LINKS</span></span>

[<span data-ttu-id="f87ef-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="f87ef-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="f87ef-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f87ef-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

