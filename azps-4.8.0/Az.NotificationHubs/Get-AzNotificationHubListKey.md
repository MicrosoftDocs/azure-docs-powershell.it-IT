---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 062d16155d4e1644e09f914a1114741e7bc5365f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192728"
---
# <span data-ttu-id="dbadb-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="dbadb-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="dbadb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbadb-102">SYNOPSIS</span></span>
<span data-ttu-id="dbadb-103">Ottiene le stringhe di connessione primarie e secondarie associate a una regola di autorizzazione dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dbadb-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="dbadb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbadb-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbadb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbadb-105">DESCRIPTION</span></span>
<span data-ttu-id="dbadb-106">Il cmdlet **Get-AzNotificationHubListKey** restituisce le stringhe di connessione primarie e secondarie della regola di autorizzazione della firma di accesso condiviso (SAS) dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dbadb-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="dbadb-107">Le regole di autorizzazione gestiscono i diritti utente per l'hub.</span><span class="sxs-lookup"><span data-stu-id="dbadb-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="dbadb-108">Ogni regola include una stringa di connessione primaria e secondaria.</span><span class="sxs-lookup"><span data-stu-id="dbadb-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="dbadb-109">Queste stringhe di connessione (URI) eseguono le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbadb-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="dbadb-110">Posizionare il puntatore degli utenti su una risorsa.</span><span class="sxs-lookup"><span data-stu-id="dbadb-110">Point users to a resource.</span></span>
- <span data-ttu-id="dbadb-111">Includere un token contenente i parametri della query.</span><span class="sxs-lookup"><span data-stu-id="dbadb-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="dbadb-112">Uno di questi parametri, la firma, viene usato per autenticare l'utente e specificare il livello di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="dbadb-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="dbadb-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbadb-113">EXAMPLES</span></span>

### <span data-ttu-id="dbadb-114">Esempio 1: ottenere le stringhe di connessione primarie e secondarie per una regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="dbadb-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="dbadb-115">Questo comando ottiene le stringhe di connessione primarie e secondarie per la regola di autorizzazione ListenRule, una regola assegnata all'hub di notifica di ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="dbadb-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="dbadb-116">Il comando deve includere lo spazio dei nomi Hub e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dbadb-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="dbadb-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbadb-117">PARAMETERS</span></span>

### <span data-ttu-id="dbadb-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dbadb-118">-AuthorizationRule</span></span>
<span data-ttu-id="dbadb-119">Specifica il nome di una regola di autenticazione SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="dbadb-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="dbadb-120">Queste regole determinano il tipo di accesso che gli utenti hanno all'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dbadb-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="dbadb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbadb-121">-DefaultProfile</span></span>
<span data-ttu-id="dbadb-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dbadb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbadb-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dbadb-123">-Namespace</span></span>
<span data-ttu-id="dbadb-124">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dbadb-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="dbadb-125">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dbadb-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="dbadb-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="dbadb-126">-NotificationHub</span></span>
<span data-ttu-id="dbadb-127">Specifica l'hub di notifica a cui questo cmdlet assegna una regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="dbadb-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="dbadb-128">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="dbadb-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="dbadb-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dbadb-129">-ResourceGroup</span></span>
<span data-ttu-id="dbadb-130">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dbadb-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="dbadb-131">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dbadb-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="dbadb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbadb-132">CommonParameters</span></span>
<span data-ttu-id="dbadb-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbadb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbadb-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbadb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbadb-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbadb-135">INPUTS</span></span>

### <span data-ttu-id="dbadb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dbadb-136">System.String</span></span>

## <span data-ttu-id="dbadb-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbadb-137">OUTPUTS</span></span>

### <span data-ttu-id="dbadb-138">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="dbadb-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="dbadb-139">Note</span><span class="sxs-lookup"><span data-stu-id="dbadb-139">NOTES</span></span>

## <span data-ttu-id="dbadb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbadb-140">RELATED LINKS</span></span>

[<span data-ttu-id="dbadb-141">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dbadb-141">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

