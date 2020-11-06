---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 340320ee102317069e81806ba9a7831dc1077368
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519441"
---
# <span data-ttu-id="525ef-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="525ef-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="525ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="525ef-102">SYNOPSIS</span></span>
<span data-ttu-id="525ef-103">Ottiene una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="525ef-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="525ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="525ef-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="525ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="525ef-105">DESCRIPTION</span></span>
<span data-ttu-id="525ef-106">Il cmdlet **Get-AzureRmIntegrationAccountMap** ottiene la mappa degli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="525ef-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="525ef-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome della mappa.</span><span class="sxs-lookup"><span data-stu-id="525ef-107">Specifying the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="525ef-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="525ef-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="525ef-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="525ef-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="525ef-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="525ef-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="525ef-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="525ef-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="525ef-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="525ef-112">EXAMPLES</span></span>

### <span data-ttu-id="525ef-113">Esempio 1: ottenere una mappa dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="525ef-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="525ef-114">Questo comando ottiene una mappa dell'account di integrazione denominata IntegrationAccountMap47 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="525ef-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="525ef-115">Esempio 2: ottenere le mappe degli account di integrazione tramite il nome dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="525ef-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="525ef-116">Questo comando consente di ottenere le mappe degli account di integrazione tramite il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="525ef-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="525ef-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="525ef-117">PARAMETERS</span></span>

### <span data-ttu-id="525ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="525ef-118">-DefaultProfile</span></span>
<span data-ttu-id="525ef-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="525ef-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="525ef-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="525ef-120">-MapName</span></span>
<span data-ttu-id="525ef-121">Specifica il nome di una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="525ef-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="525ef-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="525ef-122">-Name</span></span>
<span data-ttu-id="525ef-123">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="525ef-123">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="525ef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="525ef-124">-ResourceGroupName</span></span>
<span data-ttu-id="525ef-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="525ef-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="525ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="525ef-126">CommonParameters</span></span>
<span data-ttu-id="525ef-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="525ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="525ef-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="525ef-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="525ef-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="525ef-129">INPUTS</span></span>

### <span data-ttu-id="525ef-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="525ef-130">None</span></span>
<span data-ttu-id="525ef-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="525ef-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="525ef-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="525ef-132">OUTPUTS</span></span>

### <span data-ttu-id="525ef-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="525ef-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="525ef-134">Note</span><span class="sxs-lookup"><span data-stu-id="525ef-134">NOTES</span></span>

## <span data-ttu-id="525ef-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="525ef-135">RELATED LINKS</span></span>

[<span data-ttu-id="525ef-136">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="525ef-136">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="525ef-137">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="525ef-137">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="525ef-138">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="525ef-138">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


