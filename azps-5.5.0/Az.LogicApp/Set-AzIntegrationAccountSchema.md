---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: c43bfb5fd43df92d6b8d1674b4a856829b3258d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187558"
---
# <span data-ttu-id="4e66b-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="4e66b-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="4e66b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e66b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e66b-103">Modifica uno schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4e66b-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="4e66b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e66b-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e66b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4e66b-105">DESCRIPTION</span></span>
<span data-ttu-id="4e66b-106">Il cmdlet **Set-AzIntegrationAccountSchema** modifica uno schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4e66b-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="4e66b-107">Questo cmdlet restituisce un oggetto che rappresenta lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4e66b-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="4e66b-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="4e66b-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="4e66b-109">I valori del file di parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri di modello in un oggetto parametro modello.</span><span class="sxs-lookup"><span data-stu-id="4e66b-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="4e66b-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="4e66b-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4e66b-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="4e66b-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4e66b-112">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="4e66b-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4e66b-113">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="4e66b-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4e66b-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e66b-114">EXAMPLES</span></span>

### <span data-ttu-id="4e66b-115">Esempio 1: Modificare lo schema di un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="4e66b-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="4e66b-116">Questo comando modifica lo schema dell'account di integrazione denominato IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="4e66b-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="4e66b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e66b-117">PARAMETERS</span></span>

### <span data-ttu-id="4e66b-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="4e66b-118">-ContentType</span></span>
<span data-ttu-id="4e66b-119">Specifica un tipo di contenuto per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4e66b-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="4e66b-120">Questo cmdlet supporta l'applicazione/xml come tipo di contenuto mappa.</span><span class="sxs-lookup"><span data-stu-id="4e66b-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="4e66b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e66b-121">-DefaultProfile</span></span>
<span data-ttu-id="4e66b-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4e66b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e66b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4e66b-123">-Force</span></span>
<span data-ttu-id="4e66b-124">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="4e66b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4e66b-125">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4e66b-125">-Metadata</span></span>
<span data-ttu-id="4e66b-126">Specifica un oggetto metadati per lo schema.</span><span class="sxs-lookup"><span data-stu-id="4e66b-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="4e66b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4e66b-127">-Name</span></span>
<span data-ttu-id="4e66b-128">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4e66b-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="4e66b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e66b-129">-ResourceGroupName</span></span>
<span data-ttu-id="4e66b-130">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e66b-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4e66b-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="4e66b-131">-SchemaDefinition</span></span>
<span data-ttu-id="4e66b-132">Specifica un oggetto definizione per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4e66b-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="4e66b-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="4e66b-133">-SchemaFilePath</span></span>
<span data-ttu-id="4e66b-134">Specifica il percorso file di una definizione per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4e66b-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="4e66b-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4e66b-135">-SchemaName</span></span>
<span data-ttu-id="4e66b-136">Specifica il nome dello schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4e66b-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="4e66b-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="4e66b-137">-SchemaType</span></span>
<span data-ttu-id="4e66b-138">Specifica il tipo per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="4e66b-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="4e66b-139">Questo parametro supporta xml come tipo.</span><span class="sxs-lookup"><span data-stu-id="4e66b-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e66b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e66b-140">-Confirm</span></span>
<span data-ttu-id="4e66b-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e66b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e66b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e66b-142">-WhatIf</span></span>
<span data-ttu-id="4e66b-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e66b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e66b-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e66b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e66b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e66b-145">CommonParameters</span></span>
<span data-ttu-id="4e66b-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e66b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e66b-147">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e66b-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e66b-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="4e66b-148">INPUTS</span></span>

### <span data-ttu-id="4e66b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4e66b-149">System.String</span></span>

## <span data-ttu-id="4e66b-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e66b-150">OUTPUTS</span></span>

### <span data-ttu-id="4e66b-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="4e66b-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="4e66b-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="4e66b-152">NOTES</span></span>

## <span data-ttu-id="4e66b-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e66b-153">RELATED LINKS</span></span>

[<span data-ttu-id="4e66b-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="4e66b-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="4e66b-155">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="4e66b-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="4e66b-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="4e66b-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


