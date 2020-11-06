---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 6f1f58f5f25b3e3ef4782bcc0ea8a4b3170eed81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510543"
---
# <span data-ttu-id="a381e-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a381e-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="a381e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a381e-102">SYNOPSIS</span></span>
<span data-ttu-id="a381e-103">Ottiene una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a381e-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a381e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a381e-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a381e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a381e-105">DESCRIPTION</span></span>
<span data-ttu-id="a381e-106">Il cmdlet **Get-AzureRmIntegrationAccountMap** ottiene la mappa degli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a381e-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="a381e-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome della mappa.</span><span class="sxs-lookup"><span data-stu-id="a381e-107">Specifying the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="a381e-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="a381e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a381e-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="a381e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a381e-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="a381e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a381e-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="a381e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a381e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a381e-112">EXAMPLES</span></span>

### <span data-ttu-id="a381e-113">Esempio 1: ottenere una mappa dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="a381e-113">Example 1: Get an integration account map</span></span>
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

<span data-ttu-id="a381e-114">Questo comando ottiene una mappa dell'account di integrazione denominata IntegrationAccountMap47 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a381e-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="a381e-115">Esempio 2: ottenere le mappe degli account di integrazione tramite il nome dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="a381e-115">Example 2: Get integration account maps by integration account name</span></span>
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

<span data-ttu-id="a381e-116">Questo comando consente di ottenere le mappe degli account di integrazione tramite il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a381e-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="a381e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a381e-117">PARAMETERS</span></span>

### <span data-ttu-id="a381e-118">-MapName</span><span class="sxs-lookup"><span data-stu-id="a381e-118">-MapName</span></span>
<span data-ttu-id="a381e-119">Specifica il nome di una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a381e-119">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="a381e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a381e-120">-Name</span></span>
<span data-ttu-id="a381e-121">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="a381e-121">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="a381e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a381e-122">-ResourceGroupName</span></span>
<span data-ttu-id="a381e-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a381e-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a381e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a381e-124">-DefaultProfile</span></span>
<span data-ttu-id="a381e-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a381e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a381e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a381e-126">CommonParameters</span></span>
<span data-ttu-id="a381e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a381e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a381e-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a381e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a381e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a381e-129">INPUTS</span></span>

## <span data-ttu-id="a381e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a381e-130">OUTPUTS</span></span>

### <span data-ttu-id="a381e-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a381e-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="a381e-132">Note</span><span class="sxs-lookup"><span data-stu-id="a381e-132">NOTES</span></span>

## <span data-ttu-id="a381e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a381e-133">RELATED LINKS</span></span>

[<span data-ttu-id="a381e-134">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a381e-134">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="a381e-135">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a381e-135">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="a381e-136">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a381e-136">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


