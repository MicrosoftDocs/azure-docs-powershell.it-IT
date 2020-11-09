---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300588"
---
# <span data-ttu-id="8038d-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8038d-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="8038d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8038d-102">SYNOPSIS</span></span>
<span data-ttu-id="8038d-103">Acquisisce un gruppo di risorse come modello e lo salva in un file.</span><span class="sxs-lookup"><span data-stu-id="8038d-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="8038d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8038d-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8038d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8038d-105">DESCRIPTION</span></span>
<span data-ttu-id="8038d-106">Il cmdlet **Export-AzResourceGroup** acquisisce il gruppo di risorse specificato come modello e lo salva in un file JSON. Questo può essere utile in scenari in cui sono già state create alcune risorse nel gruppo di risorse e quindi si vogliono sfruttare i vantaggi derivanti dall'uso di distribuzioni con backup del modello.</span><span class="sxs-lookup"><span data-stu-id="8038d-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="8038d-107">Questo cmdlet consente di iniziare facilmente generando il modello per le risorse esistenti nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="8038d-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="8038d-108">In alcuni casi il cmdlet non riesce a generare alcune parti del modello.</span><span class="sxs-lookup"><span data-stu-id="8038d-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="8038d-109">I messaggi di avviso comunicheranno le risorse non riuscite.</span><span class="sxs-lookup"><span data-stu-id="8038d-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="8038d-110">Il modello verrà ancora generato per le parti che hanno avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8038d-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="8038d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8038d-111">EXAMPLES</span></span>

### <span data-ttu-id="8038d-112">Esempio 1: esportare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8038d-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="8038d-113">Questo comando acquisisce il gruppo di risorse denominato TestGroup come modello e lo salva in un file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="8038d-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="8038d-114">Esempio 2: esportare una singola risorsa da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8038d-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="8038d-115">Questo comando acquisisce la risorsa della macchina virtuale denominata "TestVirtualMachine" dal gruppo di risorse "TestGroup" come modello e la Salva in un file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="8038d-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="8038d-116">Esempio 3: esportare una selezione di risorse da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8038d-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="8038d-117">Questo comando acquisisce due risorse dal gruppo di risorse "TestGroup" come modello e la Salva in un file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="8038d-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="8038d-118">Il modello generato non conterrà parametri generati.</span><span class="sxs-lookup"><span data-stu-id="8038d-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="8038d-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8038d-119">PARAMETERS</span></span>

### <span data-ttu-id="8038d-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8038d-120">-ApiVersion</span></span>
<span data-ttu-id="8038d-121">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="8038d-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8038d-122">Se non viene specificato, viene usata la versione più recente dell'API.</span><span class="sxs-lookup"><span data-stu-id="8038d-122">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="8038d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8038d-123">-DefaultProfile</span></span>
<span data-ttu-id="8038d-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8038d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8038d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8038d-125">-Force</span></span>
<span data-ttu-id="8038d-126">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8038d-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8038d-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="8038d-127">-IncludeComments</span></span>
<span data-ttu-id="8038d-128">Indica che questa operazione Esporta il modello con i commenti.</span><span class="sxs-lookup"><span data-stu-id="8038d-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="8038d-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="8038d-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="8038d-130">Indica che questa operazione Esporta il parametro di modello con il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8038d-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="8038d-131">-Path</span><span class="sxs-lookup"><span data-stu-id="8038d-131">-Path</span></span>
<span data-ttu-id="8038d-132">Specifica il percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="8038d-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="8038d-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="8038d-133">-Pre</span></span>
<span data-ttu-id="8038d-134">Indica che questo cmdlet USA versioni dell'API di pre-rilascio quando determina automaticamente la versione dell'API da usare.</span><span class="sxs-lookup"><span data-stu-id="8038d-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="8038d-135">-Resource</span><span class="sxs-lookup"><span data-stu-id="8038d-135">-Resource</span></span>
<span data-ttu-id="8038d-136">Un elenco di resourceIds per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="8038d-136">A list of resourceIds to filter the results by.</span></span>

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

### <span data-ttu-id="8038d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8038d-137">-ResourceGroupName</span></span>
<span data-ttu-id="8038d-138">Specifica il nome del gruppo di risorse da esportare.</span><span class="sxs-lookup"><span data-stu-id="8038d-138">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="8038d-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="8038d-139">-SkipAllParameterization</span></span>
<span data-ttu-id="8038d-140">Ignorare tutte le parametrizzazione.</span><span class="sxs-lookup"><span data-stu-id="8038d-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="8038d-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="8038d-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="8038d-142">Ignorare il nome della risorsa parametrizzazione.</span><span class="sxs-lookup"><span data-stu-id="8038d-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="8038d-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8038d-143">-Confirm</span></span>
<span data-ttu-id="8038d-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8038d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8038d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8038d-145">-WhatIf</span></span>
<span data-ttu-id="8038d-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8038d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8038d-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8038d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8038d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8038d-148">CommonParameters</span></span>
<span data-ttu-id="8038d-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8038d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8038d-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8038d-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8038d-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8038d-151">INPUTS</span></span>

### <span data-ttu-id="8038d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8038d-152">System.String</span></span>

## <span data-ttu-id="8038d-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8038d-153">OUTPUTS</span></span>

### <span data-ttu-id="8038d-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8038d-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8038d-155">Note</span><span class="sxs-lookup"><span data-stu-id="8038d-155">NOTES</span></span>

## <span data-ttu-id="8038d-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8038d-156">RELATED LINKS</span></span>

[<span data-ttu-id="8038d-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8038d-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


