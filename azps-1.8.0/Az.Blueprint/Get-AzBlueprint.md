---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: e559e3804c5a89648df526ab3f4fc23f8cc70b77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684898"
---
# <span data-ttu-id="7e498-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="7e498-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="7e498-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e498-102">SYNOPSIS</span></span>
<span data-ttu-id="7e498-103">Ottenere una o più definizioni di Blueprint.</span><span class="sxs-lookup"><span data-stu-id="7e498-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="7e498-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e498-104">SYNTAX</span></span>

### <span data-ttu-id="7e498-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e498-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e498-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="7e498-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e498-107">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="7e498-107">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e498-108">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="7e498-108">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint [[-SubscriptionId] <String>] [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e498-109">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="7e498-109">ManagementGroupScope</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e498-110">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="7e498-110">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e498-111">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="7e498-111">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e498-112">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="7e498-112">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint [-ManagementGroupId] <String> [-Name] <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e498-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e498-113">DESCRIPTION</span></span>
<span data-ttu-id="7e498-114">Ottenere una o più definizioni di Blueprint.</span><span class="sxs-lookup"><span data-stu-id="7e498-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="7e498-115">Le definizioni del modello sono disponibili nel gruppo di gestione o nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7e498-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="7e498-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e498-116">EXAMPLES</span></span>

### <span data-ttu-id="7e498-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e498-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
DefinitionLocationId : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="7e498-118">Ottenere le definizioni del modello nell'abbonamento corrente e nella gerarchia del gruppo di gestione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7e498-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="7e498-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7e498-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
DefinitionLocationId : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="7e498-120">Ottenere le definizioni del progetto all'interno del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="7e498-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="7e498-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7e498-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
DefinitionLocationId : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="7e498-122">Ottenere le definizioni del modello nell'abbonamento specificato e nella gerarchia del gruppo di gestione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7e498-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="7e498-123">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="7e498-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="7e498-124">Ottenere la definizione del modello con il nome specificato all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="7e498-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="7e498-125">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="7e498-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="7e498-126">Ottenere la definizione del modello con il nome e la versione specificati nel gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="7e498-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="7e498-127">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="7e498-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="7e498-128">Ottenere l'ultima definizione del modello pubblicata con il nome specificato nel gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="7e498-128">Get the lastest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="7e498-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e498-129">PARAMETERS</span></span>

### <span data-ttu-id="7e498-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e498-130">-DefaultProfile</span></span>
<span data-ttu-id="7e498-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e498-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e498-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="7e498-132">-LatestPublished</span></span>
<span data-ttu-id="7e498-133">L'ultimo flag di definizione del modello pubblicato.</span><span class="sxs-lookup"><span data-stu-id="7e498-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="7e498-134">Quando è impostato, l'esecuzione restituisce l'ultima versione pubblicata della definizione del modello.</span><span class="sxs-lookup"><span data-stu-id="7e498-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="7e498-135">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="7e498-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySubscriptionNameAndLatestPublished, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e498-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7e498-136">-ManagementGroupId</span></span>
<span data-ttu-id="7e498-137">ID gruppo di gestione in cui viene salvata la definizione della cianografia.</span><span class="sxs-lookup"><span data-stu-id="7e498-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e498-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e498-138">-Name</span></span>
<span data-ttu-id="7e498-139">Nome definizione modello.</span><span class="sxs-lookup"><span data-stu-id="7e498-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e498-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e498-140">-SubscriptionId</span></span>
<span data-ttu-id="7e498-141">ID sottoscrizione in cui viene salvata la definizione del modello.</span><span class="sxs-lookup"><span data-stu-id="7e498-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e498-142">-Versione</span><span class="sxs-lookup"><span data-stu-id="7e498-142">-Version</span></span>
<span data-ttu-id="7e498-143">Versione di definizione del modello pubblicata.</span><span class="sxs-lookup"><span data-stu-id="7e498-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionNameAndVersion, ByManagementGroupNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e498-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e498-144">CommonParameters</span></span>
<span data-ttu-id="7e498-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e498-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e498-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e498-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e498-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e498-147">INPUTS</span></span>

### <span data-ttu-id="7e498-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7e498-148">System.String</span></span>

## <span data-ttu-id="7e498-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e498-149">OUTPUTS</span></span>

### <span data-ttu-id="7e498-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="7e498-150">System.Object</span></span>
## <span data-ttu-id="7e498-151">Note</span><span class="sxs-lookup"><span data-stu-id="7e498-151">NOTES</span></span>

## <span data-ttu-id="7e498-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e498-152">RELATED LINKS</span></span>
