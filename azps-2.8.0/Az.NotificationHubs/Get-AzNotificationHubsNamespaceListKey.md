---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 88e43b182694b50169738e0b775d9202aac15ffa
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410464"
---
# <span data-ttu-id="c69d6-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="c69d6-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="c69d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c69d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c69d6-103">Ottiene le stringhe di connessione primaria e secondaria associate a una regola di autorizzazione dello spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="c69d6-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="c69d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c69d6-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c69d6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c69d6-105">DESCRIPTION</span></span>
<span data-ttu-id="c69d6-106">Il cmdlet **Get-AzNotificationHubsNotificationListKey** restituisce le stringhe di connessione primaria e secondaria per una regola di autorizzazione della firma di accesso condiviso assegnata a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="c69d6-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="c69d6-107">Le regole di autorizzazione gestiscono i diritti utente per uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="c69d6-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="c69d6-108">Ogni regola include una stringa di connessione principale e una secondaria.</span><span class="sxs-lookup"><span data-stu-id="c69d6-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="c69d6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c69d6-109">EXAMPLES</span></span>

### <span data-ttu-id="c69d6-110">Esempio 1: Ottenere le stringhe di connessione primaria e secondaria per una regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="c69d6-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="c69d6-111">Questo comando restituisce le stringhe di connessione primaria e secondaria per la regola di autorizzazione denominata ListenRule assegnata allo spazio dei nomi Contoso Contoso Contoso.</span><span class="sxs-lookup"><span data-stu-id="c69d6-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="c69d6-112">Quando si esegue questo comando è necessario includere il nome del gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="c69d6-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="c69d6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c69d6-113">PARAMETERS</span></span>

### <span data-ttu-id="c69d6-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c69d6-114">-AuthorizationRule</span></span>
<span data-ttu-id="c69d6-115">Specifica il nome di una regola di autenticazione della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="c69d6-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="c69d6-116">Queste regole determinano il tipo di accesso all'hub di notifica a cui gli utenti hanno accesso.</span><span class="sxs-lookup"><span data-stu-id="c69d6-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="c69d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69d6-117">-DefaultProfile</span></span>
<span data-ttu-id="c69d6-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="c69d6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c69d6-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c69d6-119">-Namespace</span></span>
<span data-ttu-id="c69d6-120">Specifica lo spazio dei nomi contenente le stringhe di connessione recuperate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c69d6-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c69d6-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c69d6-121">-ResourceGroup</span></span>
<span data-ttu-id="c69d6-122">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="c69d6-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="c69d6-123">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c69d6-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="c69d6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69d6-124">CommonParameters</span></span>
<span data-ttu-id="c69d6-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c69d6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69d6-126">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c69d6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69d6-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="c69d6-127">INPUTS</span></span>

### <span data-ttu-id="c69d6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c69d6-128">System.String</span></span>

## <span data-ttu-id="c69d6-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c69d6-129">OUTPUTS</span></span>

### <span data-ttu-id="c69d6-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="c69d6-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="c69d6-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="c69d6-131">NOTES</span></span>

## <span data-ttu-id="c69d6-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c69d6-132">RELATED LINKS</span></span>

[<span data-ttu-id="c69d6-133">Get-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="c69d6-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)



