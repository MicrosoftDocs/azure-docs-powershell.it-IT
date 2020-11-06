---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: c3a30457e6fd25aa633a0faa0510ed4ce61efbd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516183"
---
# <span data-ttu-id="888af-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="888af-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="888af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="888af-102">SYNOPSIS</span></span>
<span data-ttu-id="888af-103">Crea una regola di autorizzazione e assegna la regola a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="888af-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="888af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="888af-104">SYNTAX</span></span>

### <span data-ttu-id="888af-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="888af-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="888af-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="888af-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="888af-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="888af-107">DESCRIPTION</span></span>
<span data-ttu-id="888af-108">Il cmdlet **New-AzureRmNotificationHubAuthorizationRules** crea una regola di autorizzazione della firma di accesso condiviso (SAS) dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="888af-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>

<span data-ttu-id="888af-109">Le regole di autorizzazione vengono usate per gestire l'accesso agli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="888af-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="888af-110">Questa operazione viene eseguita tramite la creazione di collegamenti, come URI, in base a livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="888af-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="888af-111">I client vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="888af-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="888af-112">Ad esempio, un client assegnato l'autorizzazione Listen verrà indirizzato all'URI per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="888af-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="888af-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="888af-113">EXAMPLES</span></span>

### <span data-ttu-id="888af-114">Esempio 1: creare una regola di autorizzazione per l'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="888af-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="888af-115">Questo comando crea una nuova regola di autorizzazione e la assegna all'hub di notifica denominato ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="888af-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="888af-116">Questo hub si trova nello spazio dei nomi ContosoNamespace ed è assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="888af-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="888af-117">Tieni presente che tutte le informazioni di configurazione per la regola, incluso il nome della regola, verranno ricavate dal file di input C:\Configuration\ExternalAccessRule.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="888af-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="888af-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="888af-118">PARAMETERS</span></span>

### <span data-ttu-id="888af-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="888af-119">-InputFile</span></span>
<span data-ttu-id="888af-120">Specifica il file di input per la regola di autorizzazione creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="888af-120">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888af-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="888af-121">-Namespace</span></span>
<span data-ttu-id="888af-122">Specifica lo spazio dei nomi a cui vengono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="888af-122">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="888af-123">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="888af-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="888af-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="888af-124">-NotificationHub</span></span>
<span data-ttu-id="888af-125">Specifica l'hub di notifica a cui verranno assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="888af-125">Specifies the notification hub that the authorization rules will be assigned to.</span></span>

<span data-ttu-id="888af-126">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="888af-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="888af-127">Tieni presente che devi specificare il nome di un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="888af-127">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="888af-128">Il cmdlet **New-AzureRmNotificationHubAuthorizationRules** non può creare nuovi hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="888af-128">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="888af-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="888af-129">-ResourceGroup</span></span>
<span data-ttu-id="888af-130">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="888af-130">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="888af-131">-SASRule</span><span class="sxs-lookup"><span data-stu-id="888af-131">-SASRule</span></span>
<span data-ttu-id="888af-132">Specifica l'oggetto **SharedAccessAuthorizationRuleAttributes** che contiene le informazioni di configurazione per le nuove regole.</span><span class="sxs-lookup"><span data-stu-id="888af-132">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888af-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="888af-133">-Confirm</span></span>
<span data-ttu-id="888af-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="888af-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888af-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="888af-135">-WhatIf</span></span>
<span data-ttu-id="888af-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="888af-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="888af-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="888af-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888af-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="888af-138">-DefaultProfile</span></span>
<span data-ttu-id="888af-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="888af-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="888af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="888af-140">CommonParameters</span></span>
<span data-ttu-id="888af-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="888af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="888af-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="888af-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="888af-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="888af-143">INPUTS</span></span>

## <span data-ttu-id="888af-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="888af-144">OUTPUTS</span></span>

### <span data-ttu-id="888af-145">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="888af-145">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="888af-146">Note</span><span class="sxs-lookup"><span data-stu-id="888af-146">NOTES</span></span>

## <span data-ttu-id="888af-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="888af-147">RELATED LINKS</span></span>

[<span data-ttu-id="888af-148">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="888af-148">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="888af-149">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="888af-149">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="888af-150">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="888af-150">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


