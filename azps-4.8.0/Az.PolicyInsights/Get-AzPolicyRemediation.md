---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44c12e08ca66c19cf3541f4abb200e1ba0663208
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192242"
---
# <span data-ttu-id="8ac70-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="8ac70-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="8ac70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ac70-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac70-103">Ottiene le correzioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="8ac70-103">Gets policy remediations.</span></span>

## <span data-ttu-id="8ac70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ac70-104">SYNTAX</span></span>

### <span data-ttu-id="8ac70-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ac70-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ac70-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8ac70-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ac70-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="8ac70-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ac70-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="8ac70-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ac70-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="8ac70-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ac70-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8ac70-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ac70-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ac70-111">DESCRIPTION</span></span>
<span data-ttu-id="8ac70-112">Il cmdlet **Get-AzPolicyRemediation** ottiene tutte le correzioni dei criteri in un ambito o una particolare correzione.</span><span class="sxs-lookup"><span data-stu-id="8ac70-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="8ac70-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ac70-113">EXAMPLES</span></span>

### <span data-ttu-id="8ac70-114">Esempio 1: ottenere tutte le correzioni dei criteri nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="8ac70-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="8ac70-115">Questo comando consente di ottenere tutte le correzioni create in corrispondenza o sotto un abbonamento denominato "abbonamento personale".</span><span class="sxs-lookup"><span data-stu-id="8ac70-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="8ac70-116">Esempio 2: ottenere una correzione dei criteri specifica e i dettagli di distribuzione</span><span class="sxs-lookup"><span data-stu-id="8ac70-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="8ac70-117">Questo comando consente di ottenere il correttivo denominato "remediation1" dal gruppo di risorse "myResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="8ac70-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="8ac70-118">Verranno inclusi i dettagli delle risorse da correggere.</span><span class="sxs-lookup"><span data-stu-id="8ac70-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="8ac70-119">Esempio 3: ottenere 10 correzioni dei criteri in un gruppo di gestione con filtri facoltativi</span><span class="sxs-lookup"><span data-stu-id="8ac70-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="8ac70-120">Questo comando ottiene un massimo di 10 correzioni dei criteri da un gruppo di gestione denominato "MG1".</span><span class="sxs-lookup"><span data-stu-id="8ac70-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="8ac70-121">Verranno recuperati solo i criteri di correzione per l'assegnazione di criteri specificata.</span><span class="sxs-lookup"><span data-stu-id="8ac70-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="8ac70-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ac70-122">PARAMETERS</span></span>

### <span data-ttu-id="8ac70-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac70-123">-DefaultProfile</span></span>
<span data-ttu-id="8ac70-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac70-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ac70-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="8ac70-125">-Filter</span></span>
<span data-ttu-id="8ac70-126">Filtrare l'espressione usando la notazione OData.</span><span class="sxs-lookup"><span data-stu-id="8ac70-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="8ac70-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="8ac70-127">-IncludeDetail</span></span>
<span data-ttu-id="8ac70-128">Includere dettagli sulle distribuzioni create dalla correzione.</span><span class="sxs-lookup"><span data-stu-id="8ac70-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="8ac70-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac70-129">-ManagementGroupName</span></span>
<span data-ttu-id="8ac70-130">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="8ac70-130">Management group ID.</span></span>

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

### <span data-ttu-id="8ac70-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ac70-131">-Name</span></span>
<span data-ttu-id="8ac70-132">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="8ac70-132">Resource name.</span></span>

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

### <span data-ttu-id="8ac70-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac70-133">-ResourceGroupName</span></span>
<span data-ttu-id="8ac70-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8ac70-134">Resource group name.</span></span>

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

### <span data-ttu-id="8ac70-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ac70-135">-ResourceId</span></span>
<span data-ttu-id="8ac70-136">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="8ac70-136">Resource ID.</span></span>

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

### <span data-ttu-id="8ac70-137">-Ambito</span><span class="sxs-lookup"><span data-stu-id="8ac70-137">-Scope</span></span>
<span data-ttu-id="8ac70-138">Ambito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8ac70-138">Scope of the resource.</span></span> <span data-ttu-id="8ac70-139">Ad esempio, "/subscriptions/{subscriptionId}/resourceGroups/{rgName}".</span><span class="sxs-lookup"><span data-stu-id="8ac70-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="8ac70-140">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="8ac70-140">-Top</span></span>
<span data-ttu-id="8ac70-141">Numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="8ac70-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="8ac70-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac70-142">CommonParameters</span></span>
<span data-ttu-id="8ac70-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac70-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac70-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ac70-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac70-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ac70-145">INPUTS</span></span>

### <span data-ttu-id="8ac70-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8ac70-146">System.String</span></span>

## <span data-ttu-id="8ac70-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ac70-147">OUTPUTS</span></span>

### <span data-ttu-id="8ac70-148">Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="8ac70-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="8ac70-149">Note</span><span class="sxs-lookup"><span data-stu-id="8ac70-149">NOTES</span></span>

## <span data-ttu-id="8ac70-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ac70-150">RELATED LINKS</span></span>
