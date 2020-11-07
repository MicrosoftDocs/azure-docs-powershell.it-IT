---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 2f6df9b28db7ad86a3c779a166df34c48d779621
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522125"
---
# <span data-ttu-id="dbc05-101">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="dbc05-101">New-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="dbc05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbc05-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc05-103">Crea una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbc05-103">Creates an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbc05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbc05-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbc05-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbc05-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc05-106">Il cmdlet **New-AzureRmIntegrationAccountMap** crea una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbc05-106">The **New-AzureRmIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="dbc05-107">Questo cmdlet restituisce un oggetto che rappresenta la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbc05-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="dbc05-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse, il nome della mappa e la definizione della mappa.</span><span class="sxs-lookup"><span data-stu-id="dbc05-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>

<span data-ttu-id="dbc05-109">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="dbc05-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="dbc05-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="dbc05-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dbc05-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="dbc05-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dbc05-112">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="dbc05-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dbc05-113">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="dbc05-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dbc05-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbc05-114">EXAMPLES</span></span>

### <span data-ttu-id="dbc05-115">Esempio 1: creare una mappa degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="dbc05-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="dbc05-116">Questo comando crea la mappa dell'account di integrazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="dbc05-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="dbc05-117">Il comando specifica una definizione di mappa archiviata nella variabile $MapContent da un comando precedente.</span><span class="sxs-lookup"><span data-stu-id="dbc05-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="dbc05-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbc05-118">PARAMETERS</span></span>

### <span data-ttu-id="dbc05-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="dbc05-119">-ContentType</span></span>
<span data-ttu-id="dbc05-120">Specifica un tipo di contenuto per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbc05-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="dbc05-121">Questo cmdlet supporta Application/XML come tipo di contenuto map.</span><span class="sxs-lookup"><span data-stu-id="dbc05-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="dbc05-122">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="dbc05-122">-MapDefinition</span></span>
<span data-ttu-id="dbc05-123">Specifica un oggetto Definition per la mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbc05-123">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="dbc05-124">Specificare questo parametro o il parametro *MapFilePath* .</span><span class="sxs-lookup"><span data-stu-id="dbc05-124">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="dbc05-125">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="dbc05-125">-MapFilePath</span></span>
<span data-ttu-id="dbc05-126">Specifica il percorso del file di una definizione per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbc05-126">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="dbc05-127">Specificare questo parametro o il parametro *MapDefinition* .</span><span class="sxs-lookup"><span data-stu-id="dbc05-127">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="dbc05-128">-MapName</span><span class="sxs-lookup"><span data-stu-id="dbc05-128">-MapName</span></span>
<span data-ttu-id="dbc05-129">Specifica un nome per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbc05-129">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="dbc05-130">-MapType</span><span class="sxs-lookup"><span data-stu-id="dbc05-130">-MapType</span></span>
<span data-ttu-id="dbc05-131">Specifica il tipo per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbc05-131">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="dbc05-132">Questo cmdlet supporta l'XSLT come tipo di mappa.</span><span class="sxs-lookup"><span data-stu-id="dbc05-132">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc05-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dbc05-133">-Metadata</span></span>
<span data-ttu-id="dbc05-134">Specifica un oggetto Metadata per la mappa.</span><span class="sxs-lookup"><span data-stu-id="dbc05-134">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="dbc05-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbc05-135">-Name</span></span>
<span data-ttu-id="dbc05-136">Specifica un nome per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbc05-136">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="dbc05-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc05-137">-ResourceGroupName</span></span>
<span data-ttu-id="dbc05-138">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dbc05-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="dbc05-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dbc05-139">-Confirm</span></span>
<span data-ttu-id="dbc05-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbc05-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbc05-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbc05-141">-WhatIf</span></span>
<span data-ttu-id="dbc05-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbc05-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbc05-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbc05-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbc05-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc05-144">-DefaultProfile</span></span>
<span data-ttu-id="dbc05-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc05-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbc05-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc05-146">CommonParameters</span></span>
<span data-ttu-id="dbc05-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc05-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc05-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc05-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc05-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbc05-149">INPUTS</span></span>

## <span data-ttu-id="dbc05-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbc05-150">OUTPUTS</span></span>

### <span data-ttu-id="dbc05-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="dbc05-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="dbc05-152">Note</span><span class="sxs-lookup"><span data-stu-id="dbc05-152">NOTES</span></span>

## <span data-ttu-id="dbc05-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbc05-153">RELATED LINKS</span></span>

[<span data-ttu-id="dbc05-154">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="dbc05-154">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="dbc05-155">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="dbc05-155">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="dbc05-156">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="dbc05-156">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)

