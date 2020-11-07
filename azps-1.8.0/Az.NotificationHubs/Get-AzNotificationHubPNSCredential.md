---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubpnscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubPNSCredential.md
ms.openlocfilehash: 440eb112ea49465863b53f705c6b90a8b2e4be74
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677865"
---
# <span data-ttu-id="c7870-101">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="c7870-101">Get-AzNotificationHubPNSCredential</span></span>

## <span data-ttu-id="c7870-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7870-102">SYNOPSIS</span></span>
<span data-ttu-id="c7870-103">Ottiene le credenziali PNS per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="c7870-103">Gets the PNS credentials for a notification hub.</span></span>

## <span data-ttu-id="c7870-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7870-104">SYNTAX</span></span>

```
Get-AzNotificationHubPNSCredential [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7870-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7870-105">DESCRIPTION</span></span>
<span data-ttu-id="c7870-106">Il cmdlet **Get-AzNotificationHubPNSCredential** ottiene le credenziali del servizio di notifica della piattaforma (PNS) per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="c7870-106">The **Get-AzNotificationHubPNSCredential** cmdlet gets the platform notification service (PNS) credentials for a notification hub.</span></span>
<span data-ttu-id="c7870-107">Ogni hub di notifica ha un singolo set di credenziali PNS.</span><span class="sxs-lookup"><span data-stu-id="c7870-107">Each notification hub has a single set of PNS credentials.</span></span>
<span data-ttu-id="c7870-108">Queste credenziali vengono applicate ai singoli servizi di notifica push, ad esempio, ma non limitati a; il servizio di notifica push di iOS, il servizio di notifica push Android e Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="c7870-108">These credentials are applied to individual push notification services such as, but not limited to; the iOS push notification service, the Android push notification service, and Windows Phone 8.</span></span>

## <span data-ttu-id="c7870-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7870-109">EXAMPLES</span></span>

### <span data-ttu-id="c7870-110">Esempio 1: ottenere le credenziali PNS per un hub di notifica specifico</span><span class="sxs-lookup"><span data-stu-id="c7870-110">Example 1: Get PNS credentials for a specific notification hub</span></span>
```
PS C:\>Get-AzNotificationHubPNSCredential -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="c7870-111">Questo comando ottiene le credenziali PNS per l'hub di notifica denominato ContosoInternalHub che appartiene al gruppo di risorse denominato ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="c7870-111">This command gets the PNS credentials for the notification hub named ContosoInternalHub that belongs to the resource group named ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="c7870-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7870-112">PARAMETERS</span></span>

### <span data-ttu-id="c7870-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7870-113">-DefaultProfile</span></span>
<span data-ttu-id="c7870-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c7870-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7870-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c7870-115">-Namespace</span></span>
<span data-ttu-id="c7870-116">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="c7870-116">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="c7870-117">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="c7870-117">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7870-118">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="c7870-118">-NotificationHub</span></span>
<span data-ttu-id="c7870-119">Specifica l'hub di notifica a cui sono assegnate le credenziali PNS.</span><span class="sxs-lookup"><span data-stu-id="c7870-119">Specifies the notification hub that the PNS credentials are assigned to.</span></span>
<span data-ttu-id="c7870-120">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="c7870-120">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7870-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c7870-121">-ResourceGroup</span></span>
<span data-ttu-id="c7870-122">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="c7870-122">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="c7870-123">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7870-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7870-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7870-124">CommonParameters</span></span>
<span data-ttu-id="c7870-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7870-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7870-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7870-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7870-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7870-127">INPUTS</span></span>

### <span data-ttu-id="c7870-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c7870-128">System.String</span></span>

## <span data-ttu-id="c7870-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7870-129">OUTPUTS</span></span>

### <span data-ttu-id="c7870-130">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="c7870-130">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="c7870-131">Note</span><span class="sxs-lookup"><span data-stu-id="c7870-131">NOTES</span></span>

## <span data-ttu-id="c7870-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7870-132">RELATED LINKS</span></span>

[<span data-ttu-id="c7870-133">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c7870-133">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)


