---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 8ad8714a59ac9f0beb0c070d5f9f89c4fbd20a43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519437"
---
# <span data-ttu-id="3da12-101">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3da12-101">Get-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="3da12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3da12-102">SYNOPSIS</span></span>
<span data-ttu-id="3da12-103">Ottiene gli schemi dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3da12-103">Gets integration account schemas.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3da12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3da12-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3da12-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3da12-105">DESCRIPTION</span></span>
<span data-ttu-id="3da12-106">Il cmdlet **Get-AzureRmIntegrationAccountSchema** ottiene gli schemi dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3da12-106">The **Get-AzureRmIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="3da12-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="3da12-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="3da12-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="3da12-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3da12-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="3da12-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3da12-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="3da12-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3da12-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="3da12-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3da12-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3da12-112">EXAMPLES</span></span>

### <span data-ttu-id="3da12-113">Esempio 1: ottenere uno schema di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="3da12-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="3da12-114">Questo comando ottiene lo schema dell'account di integrazione denominato IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="3da12-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="3da12-115">Esempio 2: ottenere gli schemi degli account di integrazione per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3da12-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="3da12-116">Questo comando consente di ottenere gli schemi dell'account di integrazione per il gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3da12-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="3da12-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3da12-117">PARAMETERS</span></span>

### <span data-ttu-id="3da12-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da12-118">-DefaultProfile</span></span>
<span data-ttu-id="3da12-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3da12-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3da12-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3da12-120">-Name</span></span>
<span data-ttu-id="3da12-121">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3da12-121">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3da12-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3da12-122">-ResourceGroupName</span></span>
<span data-ttu-id="3da12-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3da12-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3da12-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3da12-124">-SchemaName</span></span>
<span data-ttu-id="3da12-125">Specifica il nome di uno schema di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="3da12-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="3da12-126">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="3da12-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="3da12-127">.</span><span class="sxs-lookup"><span data-stu-id="3da12-127">.</span></span>

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

### <span data-ttu-id="3da12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da12-128">CommonParameters</span></span>
<span data-ttu-id="3da12-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3da12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da12-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da12-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da12-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3da12-131">INPUTS</span></span>

### <span data-ttu-id="3da12-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3da12-132">None</span></span>
<span data-ttu-id="3da12-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3da12-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3da12-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3da12-134">OUTPUTS</span></span>

### <span data-ttu-id="3da12-135">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3da12-135">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="3da12-136">Note</span><span class="sxs-lookup"><span data-stu-id="3da12-136">NOTES</span></span>

## <span data-ttu-id="3da12-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3da12-137">RELATED LINKS</span></span>

[<span data-ttu-id="3da12-138">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3da12-138">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="3da12-139">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3da12-139">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="3da12-140">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3da12-140">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


