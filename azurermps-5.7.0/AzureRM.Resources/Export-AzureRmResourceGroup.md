---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/export-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
ms.openlocfilehash: 489e1fed20231dbd4fbb20d52365e7e46b1d4230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514136"
---
# <span data-ttu-id="8c7d3-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c7d3-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="8c7d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c7d3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7d3-103">Acquisisce un gruppo di risorse come modello e lo salva in un file.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c7d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c7d3-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c7d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c7d3-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7d3-106">Il cmdlet **Export-AzureRmResourceGroup** acquisisce il gruppo di risorse specificato come modello e lo salva in un file JSON. Questo può essere utile in scenari in cui sono già state create alcune risorse nel gruppo di risorse e quindi si vogliono sfruttare i vantaggi derivanti dall'uso di distribuzioni con backup del modello.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="8c7d3-107">Questo cmdlet consente di iniziare facilmente generando il modello per le risorse esistenti nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>

<span data-ttu-id="8c7d3-108">In alcuni casi il cmdlet non riesce a generare alcune parti del modello.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="8c7d3-109">I messaggi di avviso comunicheranno le risorse non riuscite.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="8c7d3-110">Il modello verrà ancora generato per le parti che hanno avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="8c7d3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c7d3-111">EXAMPLES</span></span>

### <span data-ttu-id="8c7d3-112">Esempio 1: esportare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8c7d3-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="8c7d3-113">Questo comando acquisisce il gruppo di risorse denominato TestGroup come modello e lo salva in un file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="8c7d3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c7d3-114">PARAMETERS</span></span>

### <span data-ttu-id="8c7d3-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8c7d3-115">-ApiVersion</span></span>
<span data-ttu-id="8c7d3-116">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8c7d3-117">Se non viene specificato, viene usata la versione più recente dell'API.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-117">If not specified, the latest API version is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7d3-118">-DefaultProfile</span></span>
<span data-ttu-id="8c7d3-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8c7d3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8c7d3-120">-Force</span></span>
<span data-ttu-id="8c7d3-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="8c7d3-122">-IncludeComments</span></span>
<span data-ttu-id="8c7d3-123">Indica che questa operazione Esporta il modello con i commenti.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-123">Indicates that this operation exports the template with comments.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="8c7d3-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="8c7d3-125">Indica che questa operazione Esporta il parametro di modello con il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-125">Indicates that this operation exports the template parameter with the default value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8c7d3-126">-InformationAction</span></span>
<span data-ttu-id="8c7d3-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8c7d3-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c7d3-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c7d3-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="8c7d3-129">Continue</span></span>
- <span data-ttu-id="8c7d3-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="8c7d3-130">Ignore</span></span>
- <span data-ttu-id="8c7d3-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="8c7d3-131">Inquire</span></span>
- <span data-ttu-id="8c7d3-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8c7d3-132">SilentlyContinue</span></span>
- <span data-ttu-id="8c7d3-133">Stop</span><span class="sxs-lookup"><span data-stu-id="8c7d3-133">Stop</span></span>
- <span data-ttu-id="8c7d3-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="8c7d3-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8c7d3-135">-InformationVariable</span></span>
<span data-ttu-id="8c7d3-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-137">-Path</span><span class="sxs-lookup"><span data-stu-id="8c7d3-137">-Path</span></span>
<span data-ttu-id="8c7d3-138">Specifica il percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-138">Specifies the output path of the template file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="8c7d3-139">-Pre</span></span>
<span data-ttu-id="8c7d3-140">Indica che questo cmdlet USA versioni dell'API di pre-rilascio quando determina automaticamente la versione dell'API da usare.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-140">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c7d3-141">-ResourceGroupName</span></span>
<span data-ttu-id="8c7d3-142">Specifica il nome del gruppo di risorse da esportare.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-142">Specifies the name of the resource group to export.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8c7d3-143">-Confirm</span></span>
<span data-ttu-id="8c7d3-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c7d3-145">-WhatIf</span></span>
<span data-ttu-id="8c7d3-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c7d3-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c7d3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7d3-148">CommonParameters</span></span>
<span data-ttu-id="8c7d3-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7d3-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c7d3-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7d3-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c7d3-151">INPUTS</span></span>

### <span data-ttu-id="8c7d3-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8c7d3-152">None</span></span>
<span data-ttu-id="8c7d3-153">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8c7d3-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c7d3-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c7d3-154">OUTPUTS</span></span>

### <span data-ttu-id="8c7d3-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8c7d3-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8c7d3-156">Note</span><span class="sxs-lookup"><span data-stu-id="8c7d3-156">NOTES</span></span>

## <span data-ttu-id="8c7d3-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c7d3-157">RELATED LINKS</span></span>

[<span data-ttu-id="8c7d3-158">Trova-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c7d3-158">Find-AzureRmResourceGroup</span></span>](./Find-AzureRmResourceGroup.md)


