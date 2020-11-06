---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: cf46a3dd916bf1b28ca1c82447071cba5fd3a51d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520965"
---
# <span data-ttu-id="3ed2a-101">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3ed2a-101">Set-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="3ed2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ed2a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed2a-103">Modifica uno schema di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-103">Modifies an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ed2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ed2a-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ed2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ed2a-105">DESCRIPTION</span></span>
<span data-ttu-id="3ed2a-106">Il cmdlet **set-AzureRmIntegrationAccountSchema** modifica uno schema di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-106">The **Set-AzureRmIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="3ed2a-107">Questo cmdlet restituisce un oggetto che rappresenta lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="3ed2a-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="3ed2a-109">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="3ed2a-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3ed2a-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3ed2a-112">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3ed2a-113">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3ed2a-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ed2a-114">EXAMPLES</span></span>

### <span data-ttu-id="3ed2a-115">Esempio 1: modificare uno schema di un account di integrazione</span><span class="sxs-lookup"><span data-stu-id="3ed2a-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="3ed2a-116">Questo comando consente di modificare lo schema dell'account di integrazione denominato IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="3ed2a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ed2a-117">PARAMETERS</span></span>

### <span data-ttu-id="3ed2a-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="3ed2a-118">-ContentType</span></span>
<span data-ttu-id="3ed2a-119">Specifica un tipo di contenuto per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="3ed2a-120">Questo cmdlet supporta Application/XML come tipo di contenuto map.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="3ed2a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed2a-121">-DefaultProfile</span></span>
<span data-ttu-id="3ed2a-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3ed2a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ed2a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3ed2a-123">-Force</span></span>
<span data-ttu-id="3ed2a-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3ed2a-125">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3ed2a-125">-Metadata</span></span>
<span data-ttu-id="3ed2a-126">Specifica un oggetto Metadata per lo schema.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="3ed2a-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ed2a-127">-Name</span></span>
<span data-ttu-id="3ed2a-128">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="3ed2a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed2a-129">-ResourceGroupName</span></span>
<span data-ttu-id="3ed2a-130">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3ed2a-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="3ed2a-131">-SchemaDefinition</span></span>
<span data-ttu-id="3ed2a-132">Specifica un oggetto Definition per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="3ed2a-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="3ed2a-133">-SchemaFilePath</span></span>
<span data-ttu-id="3ed2a-134">Specifica il percorso del file di una definizione per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="3ed2a-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3ed2a-135">-SchemaName</span></span>
<span data-ttu-id="3ed2a-136">Specifica il nome dello schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="3ed2a-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="3ed2a-137">-SchemaType</span></span>
<span data-ttu-id="3ed2a-138">Specifica il tipo per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="3ed2a-139">Questo parametro supporta XML come tipo.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="3ed2a-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3ed2a-140">-Confirm</span></span>
<span data-ttu-id="3ed2a-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ed2a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ed2a-142">-WhatIf</span></span>
<span data-ttu-id="3ed2a-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ed2a-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ed2a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed2a-145">CommonParameters</span></span>
<span data-ttu-id="3ed2a-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ed2a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed2a-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ed2a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed2a-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ed2a-148">INPUTS</span></span>

### <span data-ttu-id="3ed2a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3ed2a-149">System.String</span></span>

## <span data-ttu-id="3ed2a-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ed2a-150">OUTPUTS</span></span>

### <span data-ttu-id="3ed2a-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3ed2a-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="3ed2a-152">Note</span><span class="sxs-lookup"><span data-stu-id="3ed2a-152">NOTES</span></span>

## <span data-ttu-id="3ed2a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ed2a-153">RELATED LINKS</span></span>

[<span data-ttu-id="3ed2a-154">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3ed2a-154">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="3ed2a-155">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3ed2a-155">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="3ed2a-156">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3ed2a-156">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)


