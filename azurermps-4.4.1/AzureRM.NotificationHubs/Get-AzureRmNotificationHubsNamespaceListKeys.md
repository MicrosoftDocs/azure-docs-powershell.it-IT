---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
ms.openlocfilehash: 0c834f8ee24090fa0da11f6c01fb0ddad3251756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519559"
---
# <span data-ttu-id="bb0cc-101">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="bb0cc-101">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>

## <span data-ttu-id="bb0cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0cc-103">Ottiene le stringhe di connessione primarie e secondarie associate a una regola di autorizzazione dello spazio dei nomi Hub notifica.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-103">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb0cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb0cc-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceListKeys [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb0cc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="bb0cc-106">Il cmdlet **Get-AzureRmNotificationHubsNamespaceListKeys** restituisce le stringhe di connessione primarie e secondarie per una regola di autorizzazione della firma di accesso condiviso (SAS) assegnata a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-106">The **Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet returns the primary and secondary connection strings for a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>

<span data-ttu-id="bb0cc-107">Le regole di autorizzazione gestiscono i diritti degli utenti in uno spazio dei nomi Hub notifica.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-107">Authorization rules manage user rights to a notification hub namespace.</span></span>
<span data-ttu-id="bb0cc-108">Ogni regola include una stringa di connessione primaria e secondaria.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-108">Each rule includes a primary and a secondary connection string.</span></span>

## <span data-ttu-id="bb0cc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb0cc-109">EXAMPLES</span></span>

### <span data-ttu-id="bb0cc-110">Esempio 1: ottenere le stringhe di connessione primarie e secondarie per una regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="bb0cc-110">Example 1: Get the primary and secondary connection strings for an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceListKeys -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="bb0cc-111">Questo comando restituisce le stringhe di connessione primarie e secondarie per la regola di autorizzazione denominata ListenRule assegnate allo spazio dei nomi ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-111">This command returns the primary and secondary connection strings for the authorization rule named ListenRule assigned to the ContosoNamespace namespace.</span></span>
<span data-ttu-id="bb0cc-112">Quando si esegue questo comando, è necessario includere il nome del gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-112">When you run this command you must include the name of the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="bb0cc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb0cc-113">PARAMETERS</span></span>

### <span data-ttu-id="bb0cc-114">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bb0cc-114">-AuthorizationRule</span></span>
<span data-ttu-id="bb0cc-115">Specifica il nome di una regola di autenticazione SAS.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-115">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="bb0cc-116">Queste regole determinano il tipo di accesso che gli utenti hanno all'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-116">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="bb0cc-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bb0cc-117">-Namespace</span></span>
<span data-ttu-id="bb0cc-118">Specifica lo spazio dei nomi contenente le stringhe di connessione ottenute da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-118">Specifies the namespace containing the connection strings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="bb0cc-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bb0cc-119">-ResourceGroup</span></span>
<span data-ttu-id="bb0cc-120">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-120">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="bb0cc-121">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-121">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="bb0cc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0cc-122">-DefaultProfile</span></span>
<span data-ttu-id="bb0cc-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb0cc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0cc-124">CommonParameters</span></span>
<span data-ttu-id="bb0cc-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb0cc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0cc-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb0cc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0cc-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb0cc-127">INPUTS</span></span>

## <span data-ttu-id="bb0cc-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb0cc-128">OUTPUTS</span></span>

### <span data-ttu-id="bb0cc-129">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="bb0cc-129">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="bb0cc-130">Note</span><span class="sxs-lookup"><span data-stu-id="bb0cc-130">NOTES</span></span>

## <span data-ttu-id="bb0cc-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb0cc-131">RELATED LINKS</span></span>

[<span data-ttu-id="bb0cc-132">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="bb0cc-132">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="bb0cc-133">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="bb0cc-133">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


