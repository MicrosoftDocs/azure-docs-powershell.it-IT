---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhublistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 05c6ce89577e3c24368ddf47a0dec0abfeb2a388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517395"
---
# <span data-ttu-id="8814a-101">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="8814a-101">Get-AzureRmNotificationHubListKeys</span></span>

## <span data-ttu-id="8814a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8814a-102">SYNOPSIS</span></span>
<span data-ttu-id="8814a-103">Ottiene le stringhe di connessione primarie e secondarie associate a una regola di autorizzazione dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8814a-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8814a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8814a-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8814a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8814a-105">DESCRIPTION</span></span>
<span data-ttu-id="8814a-106">Il cmdlet **Get-AzureRmNotificationHubListKeys** restituisce le stringhe di connessione primarie e secondarie della regola di autorizzazione della firma di accesso condiviso (SAS) dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8814a-106">The **Get-AzureRmNotificationHubListKeys** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="8814a-107">Le regole di autorizzazione gestiscono i diritti utente per l'hub.</span><span class="sxs-lookup"><span data-stu-id="8814a-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="8814a-108">Ogni regola include una stringa di connessione primaria e secondaria.</span><span class="sxs-lookup"><span data-stu-id="8814a-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="8814a-109">Queste stringhe di connessione (URI) eseguono le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8814a-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="8814a-110">Posizionare il puntatore degli utenti su una risorsa.</span><span class="sxs-lookup"><span data-stu-id="8814a-110">Point users to a resource.</span></span>
- <span data-ttu-id="8814a-111">Includere un token contenente i parametri della query.</span><span class="sxs-lookup"><span data-stu-id="8814a-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="8814a-112">Uno di questi parametri, la firma, viene usato per autenticare l'utente e specificare il livello di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="8814a-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="8814a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8814a-113">EXAMPLES</span></span>

### <span data-ttu-id="8814a-114">Esempio 1: ottenere le stringhe di connessione primarie e secondarie per una regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="8814a-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="8814a-115">Questo comando ottiene le stringhe di connessione primarie e secondarie per la regola di autorizzazione ListenRule, una regola assegnata all'hub di notifica di ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="8814a-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="8814a-116">Il comando deve includere lo spazio dei nomi Hub e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8814a-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="8814a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8814a-117">PARAMETERS</span></span>

### <span data-ttu-id="8814a-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8814a-118">-AuthorizationRule</span></span>
<span data-ttu-id="8814a-119">Specifica il nome di una regola di autenticazione SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="8814a-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="8814a-120">Queste regole determinano il tipo di accesso che gli utenti hanno all'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8814a-120">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8814a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8814a-121">-DefaultProfile</span></span>
<span data-ttu-id="8814a-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8814a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8814a-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8814a-123">-Namespace</span></span>
<span data-ttu-id="8814a-124">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8814a-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="8814a-125">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8814a-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8814a-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="8814a-126">-NotificationHub</span></span>
<span data-ttu-id="8814a-127">Specifica l'hub di notifica a cui questo cmdlet assegna una regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="8814a-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="8814a-128">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="8814a-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="8814a-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8814a-129">-ResourceGroup</span></span>
<span data-ttu-id="8814a-130">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8814a-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="8814a-131">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8814a-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8814a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8814a-132">CommonParameters</span></span>
<span data-ttu-id="8814a-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8814a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8814a-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8814a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8814a-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8814a-135">INPUTS</span></span>

### <span data-ttu-id="8814a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8814a-136">System.String</span></span>

## <span data-ttu-id="8814a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8814a-137">OUTPUTS</span></span>

### <span data-ttu-id="8814a-138">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="8814a-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="8814a-139">Note</span><span class="sxs-lookup"><span data-stu-id="8814a-139">NOTES</span></span>

## <span data-ttu-id="8814a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8814a-140">RELATED LINKS</span></span>

[<span data-ttu-id="8814a-141">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8814a-141">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

