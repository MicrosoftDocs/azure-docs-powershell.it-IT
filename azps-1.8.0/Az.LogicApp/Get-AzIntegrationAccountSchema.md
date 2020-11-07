---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: 9c60e9171385c915785c87d5de217b76a37a4862
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835499"
---
# <span data-ttu-id="af54b-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="af54b-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="af54b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af54b-102">SYNOPSIS</span></span>
<span data-ttu-id="af54b-103">Ottiene gli schemi dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="af54b-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="af54b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af54b-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af54b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af54b-105">DESCRIPTION</span></span>
<span data-ttu-id="af54b-106">Il cmdlet **Get-AzIntegrationAccountSchema** ottiene gli schemi dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="af54b-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="af54b-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="af54b-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="af54b-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="af54b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="af54b-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="af54b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="af54b-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="af54b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="af54b-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="af54b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="af54b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af54b-112">EXAMPLES</span></span>

### <span data-ttu-id="af54b-113">Esempio 1: ottenere uno schema di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="af54b-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
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

<span data-ttu-id="af54b-114">Questo comando ottiene lo schema dell'account di integrazione denominato IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="af54b-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="af54b-115">Esempio 2: ottenere gli schemi degli account di integrazione per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="af54b-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="af54b-116">Questo comando consente di ottenere gli schemi dell'account di integrazione per il gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="af54b-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="af54b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af54b-117">PARAMETERS</span></span>

### <span data-ttu-id="af54b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af54b-118">-DefaultProfile</span></span>
<span data-ttu-id="af54b-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="af54b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af54b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="af54b-120">-Name</span></span>
<span data-ttu-id="af54b-121">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="af54b-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af54b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af54b-122">-ResourceGroupName</span></span>
<span data-ttu-id="af54b-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af54b-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="af54b-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="af54b-124">-SchemaName</span></span>
<span data-ttu-id="af54b-125">Specifica il nome di uno schema di account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="af54b-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="af54b-126">Specifica il nome di uno schema.</span><span class="sxs-lookup"><span data-stu-id="af54b-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="af54b-127">.</span><span class="sxs-lookup"><span data-stu-id="af54b-127">.</span></span>

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

### <span data-ttu-id="af54b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af54b-128">CommonParameters</span></span>
<span data-ttu-id="af54b-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af54b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af54b-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af54b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af54b-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af54b-131">INPUTS</span></span>

### <span data-ttu-id="af54b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="af54b-132">System.String</span></span>

## <span data-ttu-id="af54b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af54b-133">OUTPUTS</span></span>

### <span data-ttu-id="af54b-134">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="af54b-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="af54b-135">Note</span><span class="sxs-lookup"><span data-stu-id="af54b-135">NOTES</span></span>

## <span data-ttu-id="af54b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af54b-136">RELATED LINKS</span></span>

[<span data-ttu-id="af54b-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="af54b-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="af54b-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="af54b-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="af54b-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="af54b-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


