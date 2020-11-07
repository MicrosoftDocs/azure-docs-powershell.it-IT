---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/export-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: a5390cd66e97f05e80f52685af6e43135ed64141
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866213"
---
# <span data-ttu-id="a4e1b-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4e1b-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="a4e1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e1b-103">Acquisisce un gruppo di risorse come modello e lo salva in un file.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4e1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4e1b-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4e1b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4e1b-105">DESCRIPTION</span></span>
<span data-ttu-id="a4e1b-106">Il cmdlet **Export-AzureRmResourceGroup** acquisisce il gruppo di risorse specificato come modello e lo salva in un file JSON. Questo può essere utile in scenari in cui sono già state create alcune risorse nel gruppo di risorse e quindi si vogliono sfruttare i vantaggi derivanti dall'uso di distribuzioni con backup del modello.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="a4e1b-107">Questo cmdlet consente di iniziare facilmente generando il modello per le risorse esistenti nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="a4e1b-108">In alcuni casi il cmdlet non riesce a generare alcune parti del modello.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="a4e1b-109">I messaggi di avviso comunicheranno le risorse non riuscite.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="a4e1b-110">Il modello verrà ancora generato per le parti che hanno avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="a4e1b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4e1b-111">EXAMPLES</span></span>

### <span data-ttu-id="a4e1b-112">Esempio 1: esportare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a4e1b-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="a4e1b-113">Questo comando acquisisce il gruppo di risorse denominato TestGroup come modello e lo salva in un file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="a4e1b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4e1b-114">PARAMETERS</span></span>

### <span data-ttu-id="a4e1b-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a4e1b-115">-ApiVersion</span></span>
<span data-ttu-id="a4e1b-116">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a4e1b-117">Se non viene specificato, viene usata la versione più recente dell'API.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="a4e1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e1b-118">-DefaultProfile</span></span>
<span data-ttu-id="a4e1b-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a4e1b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4e1b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a4e1b-120">-Force</span></span>
<span data-ttu-id="a4e1b-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4e1b-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="a4e1b-122">-IncludeComments</span></span>
<span data-ttu-id="a4e1b-123">Indica che questa operazione Esporta il modello con i commenti.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="a4e1b-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="a4e1b-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="a4e1b-125">Indica che questa operazione Esporta il parametro di modello con il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="a4e1b-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a4e1b-126">-InformationAction</span></span>
<span data-ttu-id="a4e1b-127">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="a4e1b-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4e1b-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a4e1b-129">Continuare</span><span class="sxs-lookup"><span data-stu-id="a4e1b-129">Continue</span></span>
- <span data-ttu-id="a4e1b-130">Ignora</span><span class="sxs-lookup"><span data-stu-id="a4e1b-130">Ignore</span></span>
- <span data-ttu-id="a4e1b-131">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a4e1b-131">Inquire</span></span>
- <span data-ttu-id="a4e1b-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a4e1b-132">SilentlyContinue</span></span>
- <span data-ttu-id="a4e1b-133">Stop</span><span class="sxs-lookup"><span data-stu-id="a4e1b-133">Stop</span></span>
- <span data-ttu-id="a4e1b-134">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a4e1b-134">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4e1b-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a4e1b-135">-InformationVariable</span></span>
<span data-ttu-id="a4e1b-136">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-136">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4e1b-137">-Path</span><span class="sxs-lookup"><span data-stu-id="a4e1b-137">-Path</span></span>
<span data-ttu-id="a4e1b-138">Specifica il percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-138">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="a4e1b-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="a4e1b-139">-Pre</span></span>
<span data-ttu-id="a4e1b-140">Indica che questo cmdlet USA versioni dell'API di pre-rilascio quando determina automaticamente la versione dell'API da usare.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-140">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="a4e1b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4e1b-141">-ResourceGroupName</span></span>
<span data-ttu-id="a4e1b-142">Specifica il nome del gruppo di risorse da esportare.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-142">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="a4e1b-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4e1b-143">-Confirm</span></span>
<span data-ttu-id="a4e1b-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4e1b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4e1b-145">-WhatIf</span></span>
<span data-ttu-id="a4e1b-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4e1b-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4e1b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e1b-148">CommonParameters</span></span>
<span data-ttu-id="a4e1b-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4e1b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e1b-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e1b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e1b-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4e1b-151">INPUTS</span></span>

## <span data-ttu-id="a4e1b-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4e1b-152">OUTPUTS</span></span>

## <span data-ttu-id="a4e1b-153">Note</span><span class="sxs-lookup"><span data-stu-id="a4e1b-153">NOTES</span></span>

## <span data-ttu-id="a4e1b-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4e1b-154">RELATED LINKS</span></span>




