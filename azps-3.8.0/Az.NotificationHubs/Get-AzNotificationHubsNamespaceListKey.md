---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespacelistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceListKey.md
ms.openlocfilehash: 90e617f35442470cef2d11c2de032679698ea167
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865032"
---
# <span data-ttu-id="8092a-101">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="8092a-101">Get-AzNotificationHubsNamespaceListKey</span></span>

## <span data-ttu-id="8092a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8092a-102">SYNOPSIS</span></span>
<span data-ttu-id="8092a-103">Ottiene le stringhe di connessione primarie e secondarie associate a una regola di autorizzazione dello spazio dei nomi Hub notifica.</span><span class="sxs-lookup"><span data-stu-id="8092a-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

## <span data-ttu-id="8092a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8092a-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceListKey [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8092a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8092a-105">DESCRIPTION</span></span>
<span data-ttu-id="8092a-106">Il cmdlet **Get-AzNotificationHubsNamespaceListKey** restituisce le stringhe di connessione primarie e secondarie per una regola di autorizzazione della firma di accesso condiviso (SAS) assegnata a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8092a-106">The **Get-AzNotificationHubsNamespaceListKey** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="8092a-107">Le regole di autorizzazione gestiscono i diritti degli utenti in uno spazio dei nomi Hub notifica.</span><span class="sxs-lookup"><span data-stu-id="8092a-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="8092a-108">Ogni regola include una stringa di connessione primaria e secondaria.</span><span class="sxs-lookup"><span data-stu-id="8092a-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="8092a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8092a-109">EXAMPLES</span></span>

### <span data-ttu-id="8092a-110">Esempio 1: ottenere le stringhe di connessione primarie e secondarie per una regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="8092a-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceListKey -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="8092a-111">Questo comando restituisce le stringhe di connessione primarie e secondarie per la regola di autorizzazione denominata ListenRule assegnate allo spazio dei nomi ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="8092a-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="8092a-112">Quando si esegue questo comando, è necessario includere il nome del gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8092a-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="8092a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8092a-113">PARAMETERS</span></span>

### <span data-ttu-id="8092a-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8092a-114">-AuthorizationRule</span></span>
<span data-ttu-id="8092a-115">Specifica il nome di una regola di autenticazione SAS.</span><span class="sxs-lookup"><span data-stu-id="8092a-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="8092a-116">Queste regole determinano il tipo di accesso che gli utenti hanno all'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8092a-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="8092a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8092a-117">-DefaultProfile</span></span>
<span data-ttu-id="8092a-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8092a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8092a-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8092a-119">-Namespace</span></span>
<span data-ttu-id="8092a-120">Specifica lo spazio dei nomi contenente le stringhe di connessione ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8092a-120">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8092a-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8092a-121">-ResourceGroup</span></span>
<span data-ttu-id="8092a-122">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8092a-122">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="8092a-123">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8092a-123">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8092a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8092a-124">CommonParameters</span></span>
<span data-ttu-id="8092a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8092a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8092a-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8092a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8092a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8092a-127">INPUTS</span></span>

### <span data-ttu-id="8092a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8092a-128">System.String</span></span>

## <span data-ttu-id="8092a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8092a-129">OUTPUTS</span></span>

### <span data-ttu-id="8092a-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="8092a-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="8092a-131">Note</span><span class="sxs-lookup"><span data-stu-id="8092a-131">NOTES</span></span>

## <span data-ttu-id="8092a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8092a-132">RELATED LINKS</span></span>

[<span data-ttu-id="8092a-133">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8092a-133">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="8092a-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8092a-134">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)


