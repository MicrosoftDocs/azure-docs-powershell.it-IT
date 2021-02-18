---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 9dfb3ff2f50df7a858ab8194ec86fa312501dcff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202207"
---
# <span data-ttu-id="ffc41-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="ffc41-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="ffc41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc41-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc41-103">Annulla una correzione dei criteri in corso.</span><span class="sxs-lookup"><span data-stu-id="ffc41-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="ffc41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ffc41-104">SYNTAX</span></span>

### <span data-ttu-id="ffc41-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ffc41-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc41-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ffc41-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc41-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ffc41-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc41-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ffc41-108">DESCRIPTION</span></span>
<span data-ttu-id="ffc41-109">Il cmdlet **Stop-AzPolicyRemediation** annulla una correzione dei criteri in corso.</span><span class="sxs-lookup"><span data-stu-id="ffc41-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="ffc41-110">Le distribuzioni attive verranno annullate e non verranno create nuove distribuzioni.</span><span class="sxs-lookup"><span data-stu-id="ffc41-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="ffc41-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ffc41-111">EXAMPLES</span></span>

### <span data-ttu-id="ffc41-112">Esempio 1: Annullare la correzione di un criterio nell'ambito del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ffc41-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="ffc41-113">Questo comando annulla la correzione denominata 'remediation1' nel gruppo di risorse 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="ffc41-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="ffc41-114">Esempio 2: Annullare la correzione di un gruppo di gestione tramite piping</span><span class="sxs-lookup"><span data-stu-id="ffc41-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="ffc41-115">Questo comando annulla la correzione denominata 'remediation1' nel gruppo di gestione 'mg1'.</span><span class="sxs-lookup"><span data-stu-id="ffc41-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="ffc41-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffc41-116">PARAMETERS</span></span>

### <span data-ttu-id="ffc41-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffc41-117">-AsJob</span></span>
<span data-ttu-id="ffc41-118">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="ffc41-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ffc41-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc41-119">-DefaultProfile</span></span>
<span data-ttu-id="ffc41-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ffc41-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffc41-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffc41-121">-InputObject</span></span>
<span data-ttu-id="ffc41-122">Oggetto Remediation.</span><span class="sxs-lookup"><span data-stu-id="ffc41-122">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc41-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc41-123">-ManagementGroupName</span></span>
<span data-ttu-id="ffc41-124">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="ffc41-124">Management group ID.</span></span>

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

### <span data-ttu-id="ffc41-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ffc41-125">-Name</span></span>
<span data-ttu-id="ffc41-126">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ffc41-126">Resource name.</span></span>

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

### <span data-ttu-id="ffc41-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffc41-127">-PassThru</span></span>
<span data-ttu-id="ffc41-128">Restituisce True se il comando viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ffc41-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="ffc41-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc41-129">-ResourceGroupName</span></span>
<span data-ttu-id="ffc41-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ffc41-130">Resource group name.</span></span>

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

### <span data-ttu-id="ffc41-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffc41-131">-ResourceId</span></span>
<span data-ttu-id="ffc41-132">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ffc41-132">Resource ID.</span></span>

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

### <span data-ttu-id="ffc41-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="ffc41-133">-Scope</span></span>
<span data-ttu-id="ffc41-134">Ambito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ffc41-134">Scope of the resource.</span></span>
<span data-ttu-id="ffc41-135">Ad esempio</span><span class="sxs-lookup"><span data-stu-id="ffc41-135">E.g.</span></span>
<span data-ttu-id="ffc41-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="ffc41-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="ffc41-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffc41-137">-Confirm</span></span>
<span data-ttu-id="ffc41-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffc41-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc41-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc41-139">-WhatIf</span></span>
<span data-ttu-id="ffc41-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffc41-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffc41-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ffc41-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc41-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc41-142">CommonParameters</span></span>
<span data-ttu-id="ffc41-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc41-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc41-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ffc41-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc41-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="ffc41-145">INPUTS</span></span>

### <span data-ttu-id="ffc41-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ffc41-146">System.String</span></span>

### <span data-ttu-id="ffc41-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="ffc41-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="ffc41-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ffc41-148">OUTPUTS</span></span>

### <span data-ttu-id="ffc41-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ffc41-149">System.Boolean</span></span>

## <span data-ttu-id="ffc41-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="ffc41-150">NOTES</span></span>

## <span data-ttu-id="ffc41-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ffc41-151">RELATED LINKS</span></span>
