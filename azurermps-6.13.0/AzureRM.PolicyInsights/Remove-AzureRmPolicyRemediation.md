---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/remove-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
ms.openlocfilehash: ec5becd714b034789aeeb8449a63012232c99d5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685763"
---
# <span data-ttu-id="f5aa5-101">Remove-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="f5aa5-101">Remove-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="f5aa5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="f5aa5-103">Elimina una correzione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-103">Deletes a policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5aa5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5aa5-104">SYNTAX</span></span>

### <span data-ttu-id="f5aa5-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f5aa5-105">ByName (Default)</span></span>
```
Remove-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5aa5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5aa5-106">ByResourceId</span></span>
```
Remove-AzureRmPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5aa5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f5aa5-107">ByInputObject</span></span>
```
Remove-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5aa5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5aa5-108">DESCRIPTION</span></span>
<span data-ttu-id="f5aa5-109">Il cmdlet **Remove-AzureRmPolicyRemediation** Elimina una correzione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-109">The **Remove-AzureRmPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="f5aa5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5aa5-110">EXAMPLES</span></span>

### <span data-ttu-id="f5aa5-111">Esempio 1: eliminare un criterio di correzione nell'ambito di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f5aa5-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="f5aa5-112">Questo comando Elimina il risanamento denominato "remediation1" nel gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="f5aa5-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="f5aa5-113">Esempio 2: eliminare una correzione del gruppo di gestione tramite piping</span><span class="sxs-lookup"><span data-stu-id="f5aa5-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzureRmPolicyRemediation -Confirm
```

<span data-ttu-id="f5aa5-114">Questo comando Elimina il risanamento denominato "remediation1" dal gruppo di gestione "MG1".</span><span class="sxs-lookup"><span data-stu-id="f5aa5-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="f5aa5-115">Verrà visualizzata una richiesta di conferma prima di eliminare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="f5aa5-116">Esempio 3: annullare ed eliminare una correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="f5aa5-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="f5aa5-117">Questo comando Elimina il risanamento denominato "remediation1" nel gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="f5aa5-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="f5aa5-118">Se la correzione è in corso, verrà annullata prima di essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="f5aa5-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5aa5-119">PARAMETERS</span></span>

### <span data-ttu-id="f5aa5-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="f5aa5-120">-AllowStop</span></span>
<span data-ttu-id="f5aa5-121">Consentire l'annullamento della correzione se è in corso.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="f5aa5-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5aa5-122">-AsJob</span></span>
<span data-ttu-id="f5aa5-123">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f5aa5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5aa5-124">-DefaultProfile</span></span>
<span data-ttu-id="f5aa5-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5aa5-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5aa5-126">-InputObject</span></span>
<span data-ttu-id="f5aa5-127">Oggetto di correzione.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-127">The Remediation object.</span></span>

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

### <span data-ttu-id="f5aa5-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f5aa5-128">-ManagementGroupName</span></span>
<span data-ttu-id="f5aa5-129">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-129">Management group ID.</span></span>

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

### <span data-ttu-id="f5aa5-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5aa5-130">-Name</span></span>
<span data-ttu-id="f5aa5-131">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-131">Resource name.</span></span>

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

### <span data-ttu-id="f5aa5-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5aa5-132">-PassThru</span></span>
<span data-ttu-id="f5aa5-133">Restituisce vero se il comando viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="f5aa5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5aa5-134">-ResourceGroupName</span></span>
<span data-ttu-id="f5aa5-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-135">Resource group name.</span></span>

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

### <span data-ttu-id="f5aa5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5aa5-136">-ResourceId</span></span>
<span data-ttu-id="f5aa5-137">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-137">Resource ID.</span></span>

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

### <span data-ttu-id="f5aa5-138">-Ambito</span><span class="sxs-lookup"><span data-stu-id="f5aa5-138">-Scope</span></span>
<span data-ttu-id="f5aa5-139">Ambito della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-139">Scope of the resource.</span></span>
<span data-ttu-id="f5aa5-140">Ad esempio.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-140">E.g.</span></span>
<span data-ttu-id="f5aa5-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="f5aa5-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f5aa5-142">-Confirm</span></span>
<span data-ttu-id="f5aa5-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5aa5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5aa5-144">-WhatIf</span></span>
<span data-ttu-id="f5aa5-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5aa5-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5aa5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5aa5-147">CommonParameters</span></span>
<span data-ttu-id="f5aa5-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5aa5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5aa5-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5aa5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5aa5-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5aa5-150">INPUTS</span></span>

### <span data-ttu-id="f5aa5-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f5aa5-151">System.String</span></span>

### <span data-ttu-id="f5aa5-152">Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="f5aa5-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="f5aa5-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5aa5-153">OUTPUTS</span></span>

### <span data-ttu-id="f5aa5-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5aa5-154">System.Boolean</span></span>

## <span data-ttu-id="f5aa5-155">Note</span><span class="sxs-lookup"><span data-stu-id="f5aa5-155">NOTES</span></span>

## <span data-ttu-id="f5aa5-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5aa5-156">RELATED LINKS</span></span>
