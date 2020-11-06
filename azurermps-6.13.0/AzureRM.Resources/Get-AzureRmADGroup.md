---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 8dc8188d9408c1b8e37fe44b149ceebeaf12ee4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514875"
---
# <span data-ttu-id="79ba7-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="79ba7-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="79ba7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="79ba7-103">Filtra i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79ba7-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79ba7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79ba7-104">SYNTAX</span></span>

### <span data-ttu-id="79ba7-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79ba7-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="79ba7-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="79ba7-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="79ba7-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79ba7-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="79ba7-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79ba7-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="79ba7-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79ba7-109">DESCRIPTION</span></span>
<span data-ttu-id="79ba7-110">Filtra i gruppi di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="79ba7-110">Filters active directory groups.</span></span>

## <span data-ttu-id="79ba7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79ba7-111">EXAMPLES</span></span>

### <span data-ttu-id="79ba7-112">Esempio 1-elenca tutti i gruppi di annunci</span><span class="sxs-lookup"><span data-stu-id="79ba7-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="79ba7-113">Elenca tutti i gruppi di annunci in un tenant.</span><span class="sxs-lookup"><span data-stu-id="79ba7-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="79ba7-114">Esempio 2-elenca tutti i gruppi di annunci tramite paging</span><span class="sxs-lookup"><span data-stu-id="79ba7-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="79ba7-115">Elenca i primi gruppi di annunci di 100 in un tenant.</span><span class="sxs-lookup"><span data-stu-id="79ba7-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="79ba7-116">Esempio 3-ottenere un gruppo di annunci per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="79ba7-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="79ba7-117">Ottiene un gruppo di annunci con ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="79ba7-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="79ba7-118">Esempio 4-gruppi di elenco per stringa di ricerca</span><span class="sxs-lookup"><span data-stu-id="79ba7-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="79ba7-119">Elenca tutti i gruppi di annunci il cui nome visualizzato inizia con "Joe".</span><span class="sxs-lookup"><span data-stu-id="79ba7-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="79ba7-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79ba7-120">PARAMETERS</span></span>

### <span data-ttu-id="79ba7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ba7-121">-DefaultProfile</span></span>
<span data-ttu-id="79ba7-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79ba7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79ba7-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="79ba7-123">-DisplayName</span></span>
<span data-ttu-id="79ba7-124">Il nome visualizzato del gruppo.</span><span class="sxs-lookup"><span data-stu-id="79ba7-124">The display name of the group.</span></span>

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

### <span data-ttu-id="79ba7-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="79ba7-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="79ba7-126">Usato per trovare i gruppi che iniziano con la stringa specificata.</span><span class="sxs-lookup"><span data-stu-id="79ba7-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="79ba7-127">-Primo</span><span class="sxs-lookup"><span data-stu-id="79ba7-127">-First</span></span>
<span data-ttu-id="79ba7-128">Numero massimo di oggetti da restituire.</span><span class="sxs-lookup"><span data-stu-id="79ba7-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="79ba7-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="79ba7-129">-IncludeTotalCount</span></span>
<span data-ttu-id="79ba7-130">Segnala il numero di oggetti nel set di dati.</span><span class="sxs-lookup"><span data-stu-id="79ba7-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="79ba7-131">Attualmente, questo parametro non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="79ba7-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="79ba7-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="79ba7-132">-ObjectId</span></span>
<span data-ttu-id="79ba7-133">ID oggetto del gruppo.</span><span class="sxs-lookup"><span data-stu-id="79ba7-133">Object id of the group.</span></span>

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

### <span data-ttu-id="79ba7-134">-Skip</span><span class="sxs-lookup"><span data-stu-id="79ba7-134">-Skip</span></span>
<span data-ttu-id="79ba7-135">Ignora i primi oggetti N e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="79ba7-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="79ba7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ba7-136">CommonParameters</span></span>
<span data-ttu-id="79ba7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79ba7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ba7-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79ba7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ba7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79ba7-139">INPUTS</span></span>

### <span data-ttu-id="79ba7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="79ba7-140">System.String</span></span>

### <span data-ttu-id="79ba7-141">System. Guid</span><span class="sxs-lookup"><span data-stu-id="79ba7-141">System.Guid</span></span>

## <span data-ttu-id="79ba7-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79ba7-142">OUTPUTS</span></span>

### <span data-ttu-id="79ba7-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="79ba7-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="79ba7-144">Note</span><span class="sxs-lookup"><span data-stu-id="79ba7-144">NOTES</span></span>

## <span data-ttu-id="79ba7-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79ba7-145">RELATED LINKS</span></span>

[<span data-ttu-id="79ba7-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="79ba7-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="79ba7-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="79ba7-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="79ba7-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="79ba7-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

