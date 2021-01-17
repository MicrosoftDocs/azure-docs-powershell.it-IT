---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342847"
---
# <span data-ttu-id="08b5b-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="08b5b-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="08b5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="08b5b-103">Ottiene partner account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="08b5b-103">Gets integration account partners.</span></span>

## <span data-ttu-id="08b5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08b5b-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08b5b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08b5b-105">DESCRIPTION</span></span>
<span data-ttu-id="08b5b-106">Il cmdlet **Get-AzIntegrationAccountPartner** ottiene i partner degli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="08b5b-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="08b5b-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del partner.</span><span class="sxs-lookup"><span data-stu-id="08b5b-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="08b5b-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="08b5b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="08b5b-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="08b5b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="08b5b-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="08b5b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="08b5b-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="08b5b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="08b5b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08b5b-112">EXAMPLES</span></span>

### <span data-ttu-id="08b5b-113">Esempio 1: ottenere un partner account di integrazione</span><span class="sxs-lookup"><span data-stu-id="08b5b-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="08b5b-114">Questo comando consente di ottenere il partner account di integrazione denominato IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="08b5b-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="08b5b-115">Esempio 2: ottenere i partner di un account di integrazione usando un nome dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="08b5b-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="08b5b-116">Questo comando consente di ottenere i partner dell'account di integrazione per l'account di integrazione denominato IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="08b5b-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="08b5b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08b5b-117">PARAMETERS</span></span>

### <span data-ttu-id="08b5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b5b-118">-DefaultProfile</span></span>
<span data-ttu-id="08b5b-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="08b5b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08b5b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="08b5b-120">-Name</span></span>
<span data-ttu-id="08b5b-121">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="08b5b-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="08b5b-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="08b5b-122">-PartnerName</span></span>
<span data-ttu-id="08b5b-123">Specifica il nome del partner dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="08b5b-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="08b5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08b5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="08b5b-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="08b5b-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="08b5b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b5b-126">CommonParameters</span></span>
<span data-ttu-id="08b5b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08b5b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b5b-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08b5b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b5b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08b5b-129">INPUTS</span></span>

### <span data-ttu-id="08b5b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="08b5b-130">System.String</span></span>

## <span data-ttu-id="08b5b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08b5b-131">OUTPUTS</span></span>

### <span data-ttu-id="08b5b-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="08b5b-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="08b5b-133">Note</span><span class="sxs-lookup"><span data-stu-id="08b5b-133">NOTES</span></span>

## <span data-ttu-id="08b5b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08b5b-134">RELATED LINKS</span></span>

[<span data-ttu-id="08b5b-135">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="08b5b-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="08b5b-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="08b5b-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="08b5b-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="08b5b-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


