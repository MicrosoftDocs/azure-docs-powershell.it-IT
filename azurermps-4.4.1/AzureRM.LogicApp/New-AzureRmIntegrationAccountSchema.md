---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: a9320219e05e61bcd77f15dd526ad45794bd45bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522123"
---
# <span data-ttu-id="dfb46-101">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dfb46-101">New-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="dfb46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfb46-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb46-103">Crea uno schema di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dfb46-103">Creates an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfb46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfb46-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfb46-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfb46-105">DESCRIPTION</span></span>
<span data-ttu-id="dfb46-106">Il cmdlet **New-AzureRmIntegrationAccountSchema** crea uno schema di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dfb46-106">The **New-AzureRmIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="dfb46-107">Questo cmdlet restituisce un oggetto che rappresenta lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dfb46-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="dfb46-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse, il nome dello schema e la definizione dello schema.</span><span class="sxs-lookup"><span data-stu-id="dfb46-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>

<span data-ttu-id="dfb46-109">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="dfb46-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="dfb46-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="dfb46-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dfb46-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="dfb46-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dfb46-112">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="dfb46-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dfb46-113">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="dfb46-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dfb46-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfb46-114">EXAMPLES</span></span>

### <span data-ttu-id="dfb46-115">Esempio 1: creare lo schema dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="dfb46-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="dfb46-116">Questo comando crea lo schema dell'account di integrazione denominato IntegrationAccountSchema1 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="dfb46-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="dfb46-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfb46-117">PARAMETERS</span></span>

### <span data-ttu-id="dfb46-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="dfb46-118">-ContentType</span></span>
<span data-ttu-id="dfb46-119">Specifica un tipo di contenuto per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dfb46-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="dfb46-120">Questo cmdlet supporta Application/XML come tipo di contenuto map.</span><span class="sxs-lookup"><span data-stu-id="dfb46-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="dfb46-121">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dfb46-121">-Metadata</span></span>
<span data-ttu-id="dfb46-122">Specifica un oggetto Metadata per lo schema.</span><span class="sxs-lookup"><span data-stu-id="dfb46-122">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="dfb46-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfb46-123">-Name</span></span>
<span data-ttu-id="dfb46-124">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dfb46-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="dfb46-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb46-125">-ResourceGroupName</span></span>
<span data-ttu-id="dfb46-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dfb46-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dfb46-127">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="dfb46-127">-SchemaDefinition</span></span>
<span data-ttu-id="dfb46-128">Specifica un oggetto Definition per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dfb46-128">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="dfb46-129">Specificare questo parametro o il parametro *SchemaFilePath* .</span><span class="sxs-lookup"><span data-stu-id="dfb46-129">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="dfb46-130">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="dfb46-130">-SchemaFilePath</span></span>
<span data-ttu-id="dfb46-131">Specifica il percorso del file di una definizione per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dfb46-131">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="dfb46-132">Specificare questo parametro o il parametro *SchemaDefinition* .</span><span class="sxs-lookup"><span data-stu-id="dfb46-132">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="dfb46-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="dfb46-133">-SchemaName</span></span>
<span data-ttu-id="dfb46-134">Specifica un nome per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dfb46-134">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="dfb46-135">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="dfb46-135">-SchemaType</span></span>
<span data-ttu-id="dfb46-136">Specifica il tipo per lo schema dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dfb46-136">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="dfb46-137">Questo parametro supporta XML come tipo.</span><span class="sxs-lookup"><span data-stu-id="dfb46-137">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="dfb46-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dfb46-138">-Confirm</span></span>
<span data-ttu-id="dfb46-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfb46-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfb46-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb46-140">-WhatIf</span></span>
<span data-ttu-id="dfb46-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfb46-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfb46-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfb46-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfb46-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb46-143">-DefaultProfile</span></span>
<span data-ttu-id="dfb46-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb46-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfb46-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb46-145">CommonParameters</span></span>
<span data-ttu-id="dfb46-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb46-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb46-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb46-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb46-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfb46-148">INPUTS</span></span>

## <span data-ttu-id="dfb46-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfb46-149">OUTPUTS</span></span>

### <span data-ttu-id="dfb46-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dfb46-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="dfb46-151">Note</span><span class="sxs-lookup"><span data-stu-id="dfb46-151">NOTES</span></span>

## <span data-ttu-id="dfb46-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfb46-152">RELATED LINKS</span></span>

[<span data-ttu-id="dfb46-153">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dfb46-153">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="dfb46-154">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dfb46-154">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="dfb46-155">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dfb46-155">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


