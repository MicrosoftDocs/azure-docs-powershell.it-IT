---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
ms.openlocfilehash: e69ad25800dbf6aada7111a1093b4c878f3c0f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520158"
---
# <span data-ttu-id="2cd3f-101">Get-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="2cd3f-101">Get-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="2cd3f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd3f-103">Ottiene le correzioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-103">Gets policy remediations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cd3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cd3f-104">SYNTAX</span></span>

### <span data-ttu-id="2cd3f-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2cd3f-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cd3f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2cd3f-106">ByName</span></span>
```
Get-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cd3f-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="2cd3f-107">GenericScope</span></span>
```
Get-AzureRmPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd3f-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="2cd3f-108">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd3f-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="2cd3f-109">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd3f-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2cd3f-110">ByResourceId</span></span>
```
Get-AzureRmPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cd3f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cd3f-111">DESCRIPTION</span></span>
<span data-ttu-id="2cd3f-112">Il cmdlet **Get-AzureRmPolicyRemediation** ottiene tutte le correzioni dei criteri in un ambito o una particolare correzione.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-112">The **Get-AzureRmPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="2cd3f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cd3f-113">EXAMPLES</span></span>

### <span data-ttu-id="2cd3f-114">Esempio 1: ottenere tutte le correzioni dei criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="2cd3f-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Get-AzureRmPolicyRemediation
```

<span data-ttu-id="2cd3f-115">Questo comando consente di ottenere tutte le correzioni create in corrispondenza o sotto un abbonamento denominato "abbonamento personale".</span><span class="sxs-lookup"><span data-stu-id="2cd3f-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="2cd3f-116">Esempio 2: ottenere una correzione dei criteri specifica e i dettagli di distribuzione</span><span class="sxs-lookup"><span data-stu-id="2cd3f-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="2cd3f-117">Questo comando consente di ottenere il correttivo denominato "remediation1" dal gruppo di risorse "myResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="2cd3f-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="2cd3f-118">Verranno inclusi i dettagli delle risorse da correggere.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="2cd3f-119">Esempio 3: ottenere 10 correzioni dei criteri in un gruppo di gestione con filtri facoltativi</span><span class="sxs-lookup"><span data-stu-id="2cd3f-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="2cd3f-120">Questo comando ottiene un massimo di 10 correzioni dei criteri da un gruppo di gestione denominato "MG1".</span><span class="sxs-lookup"><span data-stu-id="2cd3f-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="2cd3f-121">Verranno recuperati solo i criteri di correzione per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="2cd3f-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cd3f-122">PARAMETERS</span></span>

### <span data-ttu-id="2cd3f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd3f-123">-DefaultProfile</span></span>
<span data-ttu-id="2cd3f-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cd3f-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="2cd3f-125">-Filter</span></span>
<span data-ttu-id="2cd3f-126">Filtrare l'espressione usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-126">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, GenericScope, ManagementGroupScope, ResourceGroupScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3f-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="2cd3f-127">-IncludeDetail</span></span>
<span data-ttu-id="2cd3f-128">Includere dettagli sulle distribuzioni create dalla correzione.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-128">Include details of the deployments created by the remediation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3f-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd3f-129">-ManagementGroupName</span></span>
<span data-ttu-id="2cd3f-130">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-130">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3f-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cd3f-131">-Name</span></span>
<span data-ttu-id="2cd3f-132">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-132">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd3f-133">-ResourceGroupName</span></span>
<span data-ttu-id="2cd3f-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-134">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cd3f-135">-ResourceId</span></span>
<span data-ttu-id="2cd3f-136">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-136">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3f-137">-Ambito</span><span class="sxs-lookup"><span data-stu-id="2cd3f-137">-Scope</span></span>
<span data-ttu-id="2cd3f-138">Ambito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-138">Scope of the resource.</span></span> <span data-ttu-id="2cd3f-139">Ad esempio, "/subscriptions/{subscriptionId}/resourceGroups/{rgName}".</span><span class="sxs-lookup"><span data-stu-id="2cd3f-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GenericScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3f-140">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="2cd3f-140">-Top</span></span>
<span data-ttu-id="2cd3f-141">Numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-141">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cd3f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd3f-142">CommonParameters</span></span>
<span data-ttu-id="2cd3f-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cd3f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd3f-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cd3f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd3f-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cd3f-145">INPUTS</span></span>

### <span data-ttu-id="2cd3f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2cd3f-146">System.String</span></span>

## <span data-ttu-id="2cd3f-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cd3f-147">OUTPUTS</span></span>

### <span data-ttu-id="2cd3f-148">Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="2cd3f-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="2cd3f-149">Note</span><span class="sxs-lookup"><span data-stu-id="2cd3f-149">NOTES</span></span>

## <span data-ttu-id="2cd3f-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cd3f-150">RELATED LINKS</span></span>
