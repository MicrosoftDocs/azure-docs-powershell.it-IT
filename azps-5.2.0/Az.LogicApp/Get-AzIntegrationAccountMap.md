---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 99f6bcda0360395826dedc02e3d8b968ee23795d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364209"
---
# <span data-ttu-id="432c1-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="432c1-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="432c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="432c1-102">SYNOPSIS</span></span>
<span data-ttu-id="432c1-103">Ottiene una mappa degli account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="432c1-103">Gets an integration account map.</span></span>

## <span data-ttu-id="432c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="432c1-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="432c1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="432c1-105">DESCRIPTION</span></span>
<span data-ttu-id="432c1-106">Il cmdlet **Get-AzIntegrationAccountMap** ottiene la mappa degli account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="432c1-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="432c1-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome della mappa.</span><span class="sxs-lookup"><span data-stu-id="432c1-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="432c1-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="432c1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="432c1-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="432c1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="432c1-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="432c1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="432c1-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="432c1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="432c1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="432c1-112">EXAMPLES</span></span>

### <span data-ttu-id="432c1-113">Esempio 1: ottenere una mappa dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="432c1-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
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

<span data-ttu-id="432c1-114">Questo comando ottiene una mappa dell'account di integrazione denominata IntegrationAccountMap47 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="432c1-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="432c1-115">Esempio 2: ottenere le mappe degli account di integrazione tramite il nome dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="432c1-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="432c1-116">Questo comando consente di ottenere le mappe degli account di integrazione tramite il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="432c1-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="432c1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="432c1-117">PARAMETERS</span></span>

### <span data-ttu-id="432c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="432c1-118">-DefaultProfile</span></span>
<span data-ttu-id="432c1-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="432c1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="432c1-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="432c1-120">-MapName</span></span>
<span data-ttu-id="432c1-121">Specifica il nome di una mappa dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="432c1-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="432c1-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="432c1-122">-MapType</span></span>
<span data-ttu-id="432c1-123">Tipo di mappa account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="432c1-123">The integration account map type.</span></span>

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

### <span data-ttu-id="432c1-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="432c1-124">-Name</span></span>
<span data-ttu-id="432c1-125">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="432c1-125">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="432c1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="432c1-126">-ResourceGroupName</span></span>
<span data-ttu-id="432c1-127">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="432c1-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="432c1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="432c1-128">CommonParameters</span></span>
<span data-ttu-id="432c1-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="432c1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="432c1-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="432c1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="432c1-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="432c1-131">INPUTS</span></span>

### <span data-ttu-id="432c1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="432c1-132">System.String</span></span>

## <span data-ttu-id="432c1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="432c1-133">OUTPUTS</span></span>

### <span data-ttu-id="432c1-134">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="432c1-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="432c1-135">Note</span><span class="sxs-lookup"><span data-stu-id="432c1-135">NOTES</span></span>

## <span data-ttu-id="432c1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="432c1-136">RELATED LINKS</span></span>

[<span data-ttu-id="432c1-137">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="432c1-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="432c1-138">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="432c1-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="432c1-139">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="432c1-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


