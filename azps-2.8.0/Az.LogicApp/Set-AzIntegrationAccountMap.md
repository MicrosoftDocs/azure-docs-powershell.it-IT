---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: aa986ccb3af8cef157ad2914c722a79f8355fd55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673968"
---
# <span data-ttu-id="3932f-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3932f-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="3932f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3932f-102">SYNOPSIS</span></span>
<span data-ttu-id="3932f-103">Modifica una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3932f-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="3932f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3932f-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3932f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3932f-105">DESCRIPTION</span></span>
<span data-ttu-id="3932f-106">Il cmdlet **set-AzIntegrationAccountMap** modifica una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3932f-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="3932f-107">Questo cmdlet restituisce un oggetto che rappresenta la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3932f-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="3932f-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome della mappa.</span><span class="sxs-lookup"><span data-stu-id="3932f-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="3932f-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="3932f-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3932f-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="3932f-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3932f-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="3932f-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3932f-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="3932f-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3932f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3932f-113">EXAMPLES</span></span>

### <span data-ttu-id="3932f-114">Esempio 1: modificare una mappa dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="3932f-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="3932f-115">Questo comando modifica la mappa dell'account di integrazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="3932f-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="3932f-116">Il comando specifica una definizione di mappa archiviata nella variabile $MapContent da un comando precedente.</span><span class="sxs-lookup"><span data-stu-id="3932f-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="3932f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3932f-117">PARAMETERS</span></span>

### <span data-ttu-id="3932f-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="3932f-118">-ContentType</span></span>
<span data-ttu-id="3932f-119">Specifica un tipo di contenuto per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3932f-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="3932f-120">Questo cmdlet supporta Application/XML come tipo di contenuto map.</span><span class="sxs-lookup"><span data-stu-id="3932f-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="3932f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3932f-121">-DefaultProfile</span></span>
<span data-ttu-id="3932f-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3932f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3932f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3932f-123">-Force</span></span>
<span data-ttu-id="3932f-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3932f-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3932f-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="3932f-125">-MapDefinition</span></span>
<span data-ttu-id="3932f-126">Specifica un oggetto Definition per la mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3932f-126">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="3932f-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="3932f-127">-MapFilePath</span></span>
<span data-ttu-id="3932f-128">Specifica il percorso del file di una definizione per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3932f-128">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="3932f-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="3932f-129">-MapName</span></span>
<span data-ttu-id="3932f-130">Specifica il nome di una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3932f-130">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="3932f-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="3932f-131">-MapType</span></span>
<span data-ttu-id="3932f-132">Specifica il tipo per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3932f-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="3932f-133">Questo cmdlet supporta l'XSLT come tipo di mappa.</span><span class="sxs-lookup"><span data-stu-id="3932f-133">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="3932f-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3932f-134">-Metadata</span></span>
<span data-ttu-id="3932f-135">Specifica un oggetto Metadata per la mappa.</span><span class="sxs-lookup"><span data-stu-id="3932f-135">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="3932f-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="3932f-136">-Name</span></span>
<span data-ttu-id="3932f-137">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3932f-137">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="3932f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3932f-138">-ResourceGroupName</span></span>
<span data-ttu-id="3932f-139">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3932f-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3932f-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3932f-140">-Confirm</span></span>
<span data-ttu-id="3932f-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3932f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3932f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3932f-142">-WhatIf</span></span>
<span data-ttu-id="3932f-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3932f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3932f-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3932f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3932f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3932f-145">CommonParameters</span></span>
<span data-ttu-id="3932f-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3932f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3932f-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3932f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3932f-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3932f-148">INPUTS</span></span>

### <span data-ttu-id="3932f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3932f-149">System.String</span></span>

## <span data-ttu-id="3932f-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3932f-150">OUTPUTS</span></span>

### <span data-ttu-id="3932f-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3932f-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="3932f-152">Note</span><span class="sxs-lookup"><span data-stu-id="3932f-152">NOTES</span></span>

## <span data-ttu-id="3932f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3932f-153">RELATED LINKS</span></span>

[<span data-ttu-id="3932f-154">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3932f-154">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="3932f-155">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3932f-155">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="3932f-156">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="3932f-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


