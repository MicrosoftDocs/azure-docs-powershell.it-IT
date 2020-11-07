---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 7063fb81705a14f1c1d8f0d02a2dc51d8a5617ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686732"
---
# <span data-ttu-id="ba8ef-101">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ba8ef-101">Get-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="ba8ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8ef-103">Ottiene partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-103">Gets integration account partners.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba8ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba8ef-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba8ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba8ef-105">DESCRIPTION</span></span>
<span data-ttu-id="ba8ef-106">Il cmdlet **Get-AzureRmIntegrationAccountPartner** ottiene i partner degli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-106">The **Get-AzureRmIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="ba8ef-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="ba8ef-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ba8ef-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ba8ef-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ba8ef-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ba8ef-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba8ef-112">EXAMPLES</span></span>

### <span data-ttu-id="ba8ef-113">Esempio 1: ottenere un partner account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ba8ef-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="ba8ef-114">Questo comando consente di ottenere il partner account di integrazione denominato IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="ba8ef-115">Esempio 2: ottenere i partner di un account di integrazione usando un nome dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ba8ef-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="ba8ef-116">Questo comando consente di ottenere i partner dell'account di integrazione per l'account di integrazione denominato IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="ba8ef-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba8ef-117">PARAMETERS</span></span>

### <span data-ttu-id="ba8ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8ef-118">-DefaultProfile</span></span>
<span data-ttu-id="ba8ef-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ba8ef-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba8ef-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba8ef-120">-Name</span></span>
<span data-ttu-id="ba8ef-121">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="ba8ef-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="ba8ef-122">-PartnerName</span></span>
<span data-ttu-id="ba8ef-123">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="ba8ef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba8ef-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba8ef-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ba8ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8ef-126">CommonParameters</span></span>
<span data-ttu-id="ba8ef-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8ef-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba8ef-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8ef-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba8ef-129">INPUTS</span></span>

### <span data-ttu-id="ba8ef-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ba8ef-130">None</span></span>
<span data-ttu-id="ba8ef-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ba8ef-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba8ef-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba8ef-132">OUTPUTS</span></span>

### <span data-ttu-id="ba8ef-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ba8ef-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="ba8ef-134">Note</span><span class="sxs-lookup"><span data-stu-id="ba8ef-134">NOTES</span></span>

## <span data-ttu-id="ba8ef-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba8ef-135">RELATED LINKS</span></span>

[<span data-ttu-id="ba8ef-136">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ba8ef-136">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="ba8ef-137">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ba8ef-137">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="ba8ef-138">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ba8ef-138">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


