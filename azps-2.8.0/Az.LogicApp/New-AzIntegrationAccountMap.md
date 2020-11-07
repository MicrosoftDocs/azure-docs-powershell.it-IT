---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: e483d2f88f12655283c94d8c42e9926e4dd6cddb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674008"
---
# <span data-ttu-id="047f0-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="047f0-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="047f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="047f0-102">SYNOPSIS</span></span>
<span data-ttu-id="047f0-103">Crea una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="047f0-103">Creates an integration account map.</span></span>

## <span data-ttu-id="047f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="047f0-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="047f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="047f0-105">DESCRIPTION</span></span>
<span data-ttu-id="047f0-106">Il cmdlet **New-AzIntegrationAccountMap** crea una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="047f0-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="047f0-107">Questo cmdlet restituisce un oggetto che rappresenta la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="047f0-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="047f0-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse, il nome della mappa e la definizione della mappa.</span><span class="sxs-lookup"><span data-stu-id="047f0-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="047f0-109">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="047f0-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="047f0-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="047f0-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="047f0-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="047f0-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="047f0-112">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="047f0-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="047f0-113">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="047f0-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="047f0-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="047f0-114">EXAMPLES</span></span>

### <span data-ttu-id="047f0-115">Esempio 1: creare una mappa degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="047f0-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="047f0-116">Questo comando crea la mappa dell'account di integrazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="047f0-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="047f0-117">Il comando specifica una definizione di mappa archiviata nella variabile $MapContent da un comando precedente.</span><span class="sxs-lookup"><span data-stu-id="047f0-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="047f0-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="047f0-118">PARAMETERS</span></span>

### <span data-ttu-id="047f0-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="047f0-119">-ContentType</span></span>
<span data-ttu-id="047f0-120">Specifica un tipo di contenuto per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="047f0-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="047f0-121">Questo cmdlet supporta Application/XML come tipo di contenuto map.</span><span class="sxs-lookup"><span data-stu-id="047f0-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="047f0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="047f0-122">-DefaultProfile</span></span>
<span data-ttu-id="047f0-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="047f0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="047f0-124">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="047f0-124">-MapDefinition</span></span>
<span data-ttu-id="047f0-125">Specifica un oggetto Definition per la mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="047f0-125">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="047f0-126">Specificare questo parametro o il parametro *MapFilePath* .</span><span class="sxs-lookup"><span data-stu-id="047f0-126">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="047f0-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="047f0-127">-MapFilePath</span></span>
<span data-ttu-id="047f0-128">Specifica il percorso del file di una definizione per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="047f0-128">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="047f0-129">Specificare questo parametro o il parametro *MapDefinition* .</span><span class="sxs-lookup"><span data-stu-id="047f0-129">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="047f0-130">-MapName</span><span class="sxs-lookup"><span data-stu-id="047f0-130">-MapName</span></span>
<span data-ttu-id="047f0-131">Specifica un nome per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="047f0-131">Specifies a name for the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047f0-132">-MapType</span><span class="sxs-lookup"><span data-stu-id="047f0-132">-MapType</span></span>
<span data-ttu-id="047f0-133">Specifica il tipo per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="047f0-133">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="047f0-134">Questo cmdlet supporta l'XSLT come tipo di mappa.</span><span class="sxs-lookup"><span data-stu-id="047f0-134">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047f0-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="047f0-135">-Metadata</span></span>
<span data-ttu-id="047f0-136">Specifica un oggetto Metadata per la mappa.</span><span class="sxs-lookup"><span data-stu-id="047f0-136">Specifies a metadata object for the map.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047f0-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="047f0-137">-Name</span></span>
<span data-ttu-id="047f0-138">Specifica un nome per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="047f0-138">Specifies a name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047f0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="047f0-139">-ResourceGroupName</span></span>
<span data-ttu-id="047f0-140">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="047f0-140">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047f0-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="047f0-141">-Confirm</span></span>
<span data-ttu-id="047f0-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="047f0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="047f0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="047f0-143">-WhatIf</span></span>
<span data-ttu-id="047f0-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="047f0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="047f0-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="047f0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="047f0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047f0-146">CommonParameters</span></span>
<span data-ttu-id="047f0-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="047f0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047f0-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="047f0-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047f0-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="047f0-149">INPUTS</span></span>

### <span data-ttu-id="047f0-150">System. String</span><span class="sxs-lookup"><span data-stu-id="047f0-150">System.String</span></span>

## <span data-ttu-id="047f0-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="047f0-151">OUTPUTS</span></span>

### <span data-ttu-id="047f0-152">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="047f0-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="047f0-153">Note</span><span class="sxs-lookup"><span data-stu-id="047f0-153">NOTES</span></span>

## <span data-ttu-id="047f0-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="047f0-154">RELATED LINKS</span></span>

[<span data-ttu-id="047f0-155">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="047f0-155">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="047f0-156">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="047f0-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="047f0-157">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="047f0-157">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)

