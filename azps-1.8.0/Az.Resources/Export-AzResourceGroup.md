---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: f1801aab91887b3dd0d6a9842c7d4a6de1988a88
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "93688688"
---
# <span data-ttu-id="9bdb3-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9bdb3-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="9bdb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="9bdb3-103">Acquisisce un gruppo di risorse come modello e lo salva in un file.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="9bdb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bdb3-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bdb3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bdb3-105">DESCRIPTION</span></span>
<span data-ttu-id="9bdb3-106">Il cmdlet **Export-AzResourceGroup** acquisisce il gruppo di risorse specificato come modello e lo salva in un file JSON. Questo può essere utile in scenari in cui sono già state create alcune risorse nel gruppo di risorse e quindi si vogliono sfruttare i vantaggi derivanti dall'uso di distribuzioni con backup del modello.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="9bdb3-107">Questo cmdlet consente di iniziare facilmente generando il modello per le risorse esistenti nel gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="9bdb3-108">In alcuni casi il cmdlet non riesce a generare alcune parti del modello.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="9bdb3-109">I messaggi di avviso comunicheranno le risorse non riuscite.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="9bdb3-110">Il modello verrà ancora generato per le parti che hanno avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="9bdb3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bdb3-111">EXAMPLES</span></span>

### <span data-ttu-id="9bdb3-112">Esempio 1: esportare un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9bdb3-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="9bdb3-113">Questo comando acquisisce il gruppo di risorse denominato TestGroup come modello e lo salva in un file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="9bdb3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bdb3-114">PARAMETERS</span></span>

### <span data-ttu-id="9bdb3-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9bdb3-115">-ApiVersion</span></span>
<span data-ttu-id="9bdb3-116">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9bdb3-117">Se non viene specificato, viene usata la versione più recente dell'API.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="9bdb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bdb3-118">-DefaultProfile</span></span>
<span data-ttu-id="9bdb3-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9bdb3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bdb3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9bdb3-120">-Force</span></span>
<span data-ttu-id="9bdb3-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9bdb3-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="9bdb3-122">-IncludeComments</span></span>
<span data-ttu-id="9bdb3-123">Indica che questa operazione Esporta il modello con i commenti.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="9bdb3-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="9bdb3-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="9bdb3-125">Indica che questa operazione Esporta il parametro di modello con il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="9bdb3-126">-Path</span><span class="sxs-lookup"><span data-stu-id="9bdb3-126">-Path</span></span>
<span data-ttu-id="9bdb3-127">Specifica il percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-127">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="9bdb3-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="9bdb3-128">-Pre</span></span>
<span data-ttu-id="9bdb3-129">Indica che questo cmdlet USA versioni dell'API di pre-rilascio quando determina automaticamente la versione dell'API da usare.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-129">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="9bdb3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bdb3-130">-ResourceGroupName</span></span>
<span data-ttu-id="9bdb3-131">Specifica il nome del gruppo di risorse da esportare.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-131">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="9bdb3-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9bdb3-132">-Confirm</span></span>
<span data-ttu-id="9bdb3-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bdb3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bdb3-134">-WhatIf</span></span>
<span data-ttu-id="9bdb3-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bdb3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bdb3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bdb3-137">CommonParameters</span></span>
<span data-ttu-id="9bdb3-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bdb3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bdb3-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bdb3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bdb3-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bdb3-140">INPUTS</span></span>

### <span data-ttu-id="9bdb3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9bdb3-141">System.String</span></span>

## <span data-ttu-id="9bdb3-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bdb3-142">OUTPUTS</span></span>

### <span data-ttu-id="9bdb3-143">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9bdb3-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9bdb3-144">Note</span><span class="sxs-lookup"><span data-stu-id="9bdb3-144">NOTES</span></span>

## <span data-ttu-id="9bdb3-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bdb3-145">RELATED LINKS</span></span>

[<span data-ttu-id="9bdb3-146">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9bdb3-146">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

