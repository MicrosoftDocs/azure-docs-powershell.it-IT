---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 6b9aa676e00d137612908955e88558b4cefb0eb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677867"
---
# <span data-ttu-id="ea0b6-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="ea0b6-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="ea0b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea0b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0b6-103">Ottiene le stringhe di connessione primarie e secondarie associate a una regola di autorizzazione dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="ea0b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea0b6-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea0b6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea0b6-105">DESCRIPTION</span></span>
<span data-ttu-id="ea0b6-106">Il cmdlet **Get-AzNotificationHubListKey** restituisce le stringhe di connessione primarie e secondarie della regola di autorizzazione della firma di accesso condiviso (SAS) dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="ea0b6-107">Le regole di autorizzazione gestiscono i diritti utente per l'hub.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="ea0b6-108">Ogni regola include una stringa di connessione primaria e secondaria.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="ea0b6-109">Queste stringhe di connessione (URI) eseguono le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ea0b6-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="ea0b6-110">Posizionare il puntatore degli utenti su una risorsa.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-110">Point users to a resource.</span></span>
- <span data-ttu-id="ea0b6-111">Includere un token contenente i parametri della query.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="ea0b6-112">Uno di questi parametri, la firma, viene usato per autenticare l'utente e specificare il livello di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="ea0b6-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea0b6-113">EXAMPLES</span></span>

### <span data-ttu-id="ea0b6-114">Esempio 1: ottenere le stringhe di connessione primarie e secondarie per una regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="ea0b6-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="ea0b6-115">Questo comando ottiene le stringhe di connessione primarie e secondarie per la regola di autorizzazione ListenRule, una regola assegnata all'hub di notifica di ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="ea0b6-116">Il comando deve includere lo spazio dei nomi Hub e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="ea0b6-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea0b6-117">PARAMETERS</span></span>

### <span data-ttu-id="ea0b6-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ea0b6-118">-AuthorizationRule</span></span>
<span data-ttu-id="ea0b6-119">Specifica il nome di una regola di autenticazione SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="ea0b6-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="ea0b6-120">Queste regole determinano il tipo di accesso che gli utenti hanno all'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="ea0b6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0b6-121">-DefaultProfile</span></span>
<span data-ttu-id="ea0b6-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ea0b6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea0b6-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ea0b6-123">-Namespace</span></span>
<span data-ttu-id="ea0b6-124">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="ea0b6-125">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ea0b6-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="ea0b6-126">-NotificationHub</span></span>
<span data-ttu-id="ea0b6-127">Specifica l'hub di notifica a cui questo cmdlet assegna una regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="ea0b6-128">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="ea0b6-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea0b6-129">-ResourceGroup</span></span>
<span data-ttu-id="ea0b6-130">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="ea0b6-131">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ea0b6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0b6-132">CommonParameters</span></span>
<span data-ttu-id="ea0b6-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0b6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0b6-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0b6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0b6-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea0b6-135">INPUTS</span></span>

### <span data-ttu-id="ea0b6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ea0b6-136">System.String</span></span>

## <span data-ttu-id="ea0b6-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea0b6-137">OUTPUTS</span></span>

### <span data-ttu-id="ea0b6-138">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="ea0b6-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="ea0b6-139">Note</span><span class="sxs-lookup"><span data-stu-id="ea0b6-139">NOTES</span></span>

## <span data-ttu-id="ea0b6-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea0b6-140">RELATED LINKS</span></span>

[<span data-ttu-id="ea0b6-141">Get-AzNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="ea0b6-141">Get-AzNotificationHubAuthorizationRules</span></span>](./Get-AzNotificationHubAuthorizationRules.md)

