---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: f963a89e6220e8154c2ba958adca318036c53474
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972734"
---
# <span data-ttu-id="b5c1b-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b5c1b-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="b5c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c1b-103">Modifica una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="b5c1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5c1b-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5c1b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c1b-106">Il cmdlet **Set-AzIntegrationAccountMap** modifica una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="b5c1b-107">Questo cmdlet restituisce un oggetto che rappresenta la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="b5c1b-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome della mappa.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="b5c1b-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b5c1b-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b5c1b-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b5c1b-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b5c1b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5c1b-113">EXAMPLES</span></span>

### <span data-ttu-id="b5c1b-114">Esempio 1: Modificare una mappa di un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="b5c1b-114">Example 1: Modify an integration account map</span></span>
```powershell
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

<span data-ttu-id="b5c1b-115">Questo comando modifica la mappa dell'account di integrazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="b5c1b-116">Il comando specifica una definizione di mappa archiviata nella variabile $MapContent da un comando precedente.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="b5c1b-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b5c1b-117">Example 2</span></span>

<span data-ttu-id="b5c1b-118">Modifica una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-118">Modifies an integration account map.</span></span> <span data-ttu-id="b5c1b-119">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="b5c1b-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="b5c1b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5c1b-120">PARAMETERS</span></span>

### <span data-ttu-id="b5c1b-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="b5c1b-121">-ContentType</span></span>
<span data-ttu-id="b5c1b-122">Specifica un tipo di contenuto per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="b5c1b-123">Questo cmdlet supporta l'applicazione/xml come tipo di contenuto mappa.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="b5c1b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c1b-124">-DefaultProfile</span></span>
<span data-ttu-id="b5c1b-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b5c1b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5c1b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="b5c1b-126">-Force</span></span>
<span data-ttu-id="b5c1b-127">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5c1b-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="b5c1b-128">-MapDefinition</span></span>
<span data-ttu-id="b5c1b-129">Specifica un oggetto definizione per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="b5c1b-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="b5c1b-130">-MapFilePath</span></span>
<span data-ttu-id="b5c1b-131">Specifica il percorso file di una definizione per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="b5c1b-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="b5c1b-132">-MapName</span></span>
<span data-ttu-id="b5c1b-133">Specifica il nome di una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="b5c1b-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="b5c1b-134">-MapType</span></span>
<span data-ttu-id="b5c1b-135">Specifica il tipo per la mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="b5c1b-136">Questo cmdlet supporta Xslt come tipo di mappa.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-136">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="b5c1b-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b5c1b-137">-Metadata</span></span>
<span data-ttu-id="b5c1b-138">Specifica un oggetto metadati per la mappa.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="b5c1b-139">-Name</span><span class="sxs-lookup"><span data-stu-id="b5c1b-139">-Name</span></span>
<span data-ttu-id="b5c1b-140">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-140">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="b5c1b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c1b-141">-ResourceGroupName</span></span>
<span data-ttu-id="b5c1b-142">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b5c1b-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5c1b-143">-Confirm</span></span>
<span data-ttu-id="b5c1b-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5c1b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c1b-145">-WhatIf</span></span>
<span data-ttu-id="b5c1b-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5c1b-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5c1b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c1b-148">CommonParameters</span></span>
<span data-ttu-id="b5c1b-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c1b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c1b-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c1b-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c1b-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5c1b-151">INPUTS</span></span>

### <span data-ttu-id="b5c1b-152">System.String</span><span class="sxs-lookup"><span data-stu-id="b5c1b-152">System.String</span></span>

## <span data-ttu-id="b5c1b-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5c1b-153">OUTPUTS</span></span>

### <span data-ttu-id="b5c1b-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b5c1b-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="b5c1b-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5c1b-155">NOTES</span></span>

## <span data-ttu-id="b5c1b-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5c1b-156">RELATED LINKS</span></span>

[<span data-ttu-id="b5c1b-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b5c1b-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="b5c1b-158">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b5c1b-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="b5c1b-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b5c1b-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


