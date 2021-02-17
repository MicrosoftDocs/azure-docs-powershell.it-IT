---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 81e246162fc6c28cb23fa3015f92e43116759b4b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413286"
---
# <span data-ttu-id="008fb-101">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="008fb-101">Get-AzNotificationHubListKey</span></span>

## <span data-ttu-id="008fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="008fb-102">SYNOPSIS</span></span>
<span data-ttu-id="008fb-103">Ottiene le stringhe di connessione primaria e secondaria associate a una regola di autorizzazione dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="008fb-103">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

## <span data-ttu-id="008fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="008fb-104">SYNTAX</span></span>

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="008fb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="008fb-105">DESCRIPTION</span></span>
<span data-ttu-id="008fb-106">Il cmdlet **Get-AzNotificationHubListKey** restituisce le stringhe di connessione primaria e secondaria di una regola di autorizzazione Firma di accesso condiviso dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="008fb-106">The **Get-AzNotificationHubListKey** cmdlet returns the primary and secondary connection strings of a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="008fb-107">Le regole di autorizzazione gestiscono i diritti utente per l'hub.</span><span class="sxs-lookup"><span data-stu-id="008fb-107">Authorization rules manage user rights to the hub.</span></span>
<span data-ttu-id="008fb-108">Ogni regola include una stringa di connessione principale e una secondaria.</span><span class="sxs-lookup"><span data-stu-id="008fb-108">Each rule includes a primary and a secondary connection string.</span></span>
<span data-ttu-id="008fb-109">Queste stringhe di connessione (URI) eseguono le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="008fb-109">These connection strings (URIs) perform the following:</span></span>
- <span data-ttu-id="008fb-110">Puntare gli utenti a una risorsa.</span><span class="sxs-lookup"><span data-stu-id="008fb-110">Point users to a resource.</span></span>
- <span data-ttu-id="008fb-111">Includere un token contenente parametri di query.</span><span class="sxs-lookup"><span data-stu-id="008fb-111">Include a token containing query parameters.</span></span>
<span data-ttu-id="008fb-112">Uno di questi parametri, la firma, viene usato per autenticare l'utente e fornire il livello di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="008fb-112">One of these parameters, the signature, is used to authenticate the user and provide the specified level of access.</span></span>

## <span data-ttu-id="008fb-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="008fb-113">EXAMPLES</span></span>

### <span data-ttu-id="008fb-114">Esempio 1: Ottenere le stringhe di connessione primaria e secondaria per una regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="008fb-114">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="008fb-115">Questo comando ottiene le stringhe di connessione primaria e secondaria per la regola di autorizzazione ListenRule, una regola assegnata all'hub di notifica ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="008fb-115">This command gets the primary and secondary connection strings for the authorization rule ListenRule, a rule assigned to the ContosoInternalHub notification hub.</span></span>
<span data-ttu-id="008fb-116">Il comando deve includere lo spazio dei nomi e il gruppo di risorse dell'hub.</span><span class="sxs-lookup"><span data-stu-id="008fb-116">The command must include the hub namespace and resource group.</span></span>

## <span data-ttu-id="008fb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="008fb-117">PARAMETERS</span></span>

### <span data-ttu-id="008fb-118">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="008fb-118">-AuthorizationRule</span></span>
<span data-ttu-id="008fb-119">Specifica il nome di una regola di autenticazione della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="008fb-119">Specifies the name of a Shared Access Signature (SAS) authentication rule.</span></span>
<span data-ttu-id="008fb-120">Queste regole determinano il tipo di accesso all'hub di notifica a cui gli utenti hanno accesso.</span><span class="sxs-lookup"><span data-stu-id="008fb-120">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="008fb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008fb-121">-DefaultProfile</span></span>
<span data-ttu-id="008fb-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="008fb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="008fb-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="008fb-123">-Namespace</span></span>
<span data-ttu-id="008fb-124">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="008fb-124">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="008fb-125">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="008fb-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="008fb-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="008fb-126">-NotificationHub</span></span>
<span data-ttu-id="008fb-127">Specifica l'hub di notifica a cui questo cmdlet assegna una regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="008fb-127">Specifies the notification hub that this cmdlet assigns an authorization rule to.</span></span>
<span data-ttu-id="008fb-128">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma usata da tali client.</span><span class="sxs-lookup"><span data-stu-id="008fb-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="008fb-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="008fb-129">-ResourceGroup</span></span>
<span data-ttu-id="008fb-130">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="008fb-130">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="008fb-131">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="008fb-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="008fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008fb-132">CommonParameters</span></span>
<span data-ttu-id="008fb-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="008fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008fb-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="008fb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008fb-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="008fb-135">INPUTS</span></span>

### <span data-ttu-id="008fb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="008fb-136">System.String</span></span>

## <span data-ttu-id="008fb-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="008fb-137">OUTPUTS</span></span>

### <span data-ttu-id="008fb-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="008fb-138">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="008fb-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="008fb-139">NOTES</span></span>

## <span data-ttu-id="008fb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="008fb-140">RELATED LINKS</span></span>



