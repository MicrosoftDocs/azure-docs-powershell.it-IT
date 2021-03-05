---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 1f4f518cb203414392fe8d3f01fc0031be7f79e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974493"
---
# <span data-ttu-id="38a80-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38a80-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="38a80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38a80-102">SYNOPSIS</span></span>
<span data-ttu-id="38a80-103">Acquisisce un gruppo di risorse come modello e lo salva in un file.</span><span class="sxs-lookup"><span data-stu-id="38a80-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="38a80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38a80-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38a80-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38a80-105">DESCRIPTION</span></span>
<span data-ttu-id="38a80-106">Il cmdlet **Export-AzResourceGroup** acquisisce il gruppo di risorse specificato come modello e lo salva in un file JSON. Ciò può risultare utile in scenari in cui sono già state create alcune risorse nel gruppo di risorse e quindi si vogliono sfruttare i vantaggi derivanti dall'uso di distribuzioni con modello supportato.</span><span class="sxs-lookup"><span data-stu-id="38a80-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="38a80-107">Questo cmdlet consente di creare facilmente il modello per le risorse esistenti nel gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38a80-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="38a80-108">In alcuni casi, questo cmdlet potrebbe non generare alcune parti del modello.</span><span class="sxs-lookup"><span data-stu-id="38a80-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="38a80-109">I messaggi di avviso informano dell'esito negativo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="38a80-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="38a80-110">Il modello verrà comunque generato per le parti che hanno avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="38a80-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="38a80-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38a80-111">EXAMPLES</span></span>

### <span data-ttu-id="38a80-112">Esempio 1: Esportare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="38a80-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="38a80-113">Questo comando acquisisce il gruppo di risorse denominato Gruppo di test come modello e lo salva in un file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="38a80-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="38a80-114">Esempio 2: Esportare una singola risorsa da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="38a80-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="38a80-115">Questo comando acquisisce la risorsa macchina virtuale denominata "TestVirtualMachine" dal gruppo di risorse "TestGroup" come modello e la salva in un file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="38a80-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="38a80-116">Esempio 3: Esportare una selezione di risorse da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="38a80-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="38a80-117">Questo comando acquisisce due risorse dal gruppo di risorse "Gruppo di test" come modello e lo salva in un file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="38a80-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="38a80-118">Il modello generato non conterrà parametri generati.</span><span class="sxs-lookup"><span data-stu-id="38a80-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="38a80-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38a80-119">PARAMETERS</span></span>

### <span data-ttu-id="38a80-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="38a80-120">-ApiVersion</span></span>
<span data-ttu-id="38a80-121">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="38a80-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="38a80-122">Se non viene specificato, viene usata la versione più recente dell'API.</span><span class="sxs-lookup"><span data-stu-id="38a80-122">If not specified, the latest API version is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a80-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a80-123">-DefaultProfile</span></span>
<span data-ttu-id="38a80-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="38a80-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38a80-125">-Force</span><span class="sxs-lookup"><span data-stu-id="38a80-125">-Force</span></span>
<span data-ttu-id="38a80-126">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="38a80-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38a80-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="38a80-127">-IncludeComments</span></span>
<span data-ttu-id="38a80-128">Indica che questa operazione esporta il modello con commenti.</span><span class="sxs-lookup"><span data-stu-id="38a80-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="38a80-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="38a80-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="38a80-130">Indica che questa operazione esporta il parametro del modello con il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="38a80-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="38a80-131">-Path</span><span class="sxs-lookup"><span data-stu-id="38a80-131">-Path</span></span>
<span data-ttu-id="38a80-132">Specifica il percorso di output del file modello.</span><span class="sxs-lookup"><span data-stu-id="38a80-132">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a80-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="38a80-133">-Pre</span></span>
<span data-ttu-id="38a80-134">Indica che questo cmdlet usa versioni delle API non ancora rilasciate per determinare automaticamente la versione dell'API da usare.</span><span class="sxs-lookup"><span data-stu-id="38a80-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="38a80-135">-Risorsa</span><span class="sxs-lookup"><span data-stu-id="38a80-135">-Resource</span></span>
<span data-ttu-id="38a80-136">Elenco degli ID risorsa in base a cui filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="38a80-136">A list of resourceIds to filter the results by.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a80-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a80-137">-ResourceGroupName</span></span>
<span data-ttu-id="38a80-138">Specifica il nome del gruppo di risorse da esportare.</span><span class="sxs-lookup"><span data-stu-id="38a80-138">Specifies the name of the resource group to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38a80-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="38a80-139">-SkipAllParameterization</span></span>
<span data-ttu-id="38a80-140">Ignorare tutte le parametrizzazioni.</span><span class="sxs-lookup"><span data-stu-id="38a80-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="38a80-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="38a80-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="38a80-142">Ignorare i parametri dei nomi delle risorse.</span><span class="sxs-lookup"><span data-stu-id="38a80-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="38a80-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38a80-143">-Confirm</span></span>
<span data-ttu-id="38a80-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38a80-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a80-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a80-145">-WhatIf</span></span>
<span data-ttu-id="38a80-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38a80-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38a80-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38a80-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a80-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a80-148">CommonParameters</span></span>
<span data-ttu-id="38a80-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a80-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a80-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38a80-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a80-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="38a80-151">INPUTS</span></span>

### <span data-ttu-id="38a80-152">System.String</span><span class="sxs-lookup"><span data-stu-id="38a80-152">System.String</span></span>

## <span data-ttu-id="38a80-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38a80-153">OUTPUTS</span></span>

### <span data-ttu-id="38a80-154">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="38a80-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="38a80-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="38a80-155">NOTES</span></span>

## <span data-ttu-id="38a80-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38a80-156">RELATED LINKS</span></span>

[<span data-ttu-id="38a80-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38a80-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


