---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: c43af517065eb73e704c7672005cf81cf5a5844c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688067"
---
# <span data-ttu-id="fdc48-101">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fdc48-101">New-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="fdc48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdc48-102">SYNOPSIS</span></span>
<span data-ttu-id="fdc48-103">Crea una regola di autorizzazione e assegna la regola a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fdc48-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdc48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdc48-104">SYNTAX</span></span>

### <span data-ttu-id="fdc48-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdc48-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdc48-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdc48-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdc48-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdc48-107">DESCRIPTION</span></span>
<span data-ttu-id="fdc48-108">Il cmdlet **New-AzureRmNotificationHubAuthorizationRules** crea una regola di autorizzazione della firma di accesso condiviso (SAS) dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fdc48-108">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="fdc48-109">Le regole di autorizzazione vengono usate per gestire l'accesso agli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fdc48-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="fdc48-110">Questa operazione viene eseguita tramite la creazione di collegamenti, come URI, in base a livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="fdc48-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="fdc48-111">I client vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="fdc48-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="fdc48-112">Ad esempio, un client assegnato l'autorizzazione Listen verrà indirizzato all'URI per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="fdc48-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="fdc48-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdc48-113">EXAMPLES</span></span>

### <span data-ttu-id="fdc48-114">Esempio 1: creare una regola di autorizzazione per l'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="fdc48-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="fdc48-115">Questo comando crea una nuova regola di autorizzazione e la assegna all'hub di notifica denominato ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="fdc48-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="fdc48-116">Questo hub si trova nello spazio dei nomi ContosoNamespace ed è assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="fdc48-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="fdc48-117">Tieni presente che tutte le informazioni di configurazione per la regola, incluso il nome della regola, verranno ricavate dal file di input C:\Configuration\ExternalAccessRule.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="fdc48-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="fdc48-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdc48-118">PARAMETERS</span></span>

### <span data-ttu-id="fdc48-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdc48-119">-DefaultProfile</span></span>
<span data-ttu-id="fdc48-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fdc48-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdc48-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="fdc48-121">-InputFile</span></span>
<span data-ttu-id="fdc48-122">Specifica il file di input per la regola di autorizzazione creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdc48-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fdc48-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fdc48-123">-Namespace</span></span>
<span data-ttu-id="fdc48-124">Specifica lo spazio dei nomi a cui vengono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="fdc48-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="fdc48-125">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fdc48-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="fdc48-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="fdc48-126">-NotificationHub</span></span>
<span data-ttu-id="fdc48-127">Specifica l'hub di notifica a cui verranno assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="fdc48-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="fdc48-128">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="fdc48-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="fdc48-129">Tieni presente che devi specificare il nome di un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="fdc48-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="fdc48-130">Il cmdlet **New-AzureRmNotificationHubAuthorizationRules** non può creare nuovi hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fdc48-130">The **New-AzureRmNotificationHubAuthorizationRules** cmdlet cannot create new notification hubs.</span></span>

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

### <span data-ttu-id="fdc48-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fdc48-131">-ResourceGroup</span></span>
<span data-ttu-id="fdc48-132">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fdc48-132">Specifies the resource group that the notification hub is assigned to.</span></span>

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

### <span data-ttu-id="fdc48-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="fdc48-133">-SASRule</span></span>
<span data-ttu-id="fdc48-134">Specifica l'oggetto **SharedAccessAuthorizationRuleAttributes** che contiene le informazioni di configurazione per le nuove regole.</span><span class="sxs-lookup"><span data-stu-id="fdc48-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="fdc48-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fdc48-135">-Confirm</span></span>
<span data-ttu-id="fdc48-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdc48-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdc48-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdc48-137">-WhatIf</span></span>
<span data-ttu-id="fdc48-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdc48-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdc48-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdc48-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdc48-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdc48-140">CommonParameters</span></span>
<span data-ttu-id="fdc48-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdc48-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdc48-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdc48-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdc48-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdc48-143">INPUTS</span></span>

### <span data-ttu-id="fdc48-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fdc48-144">System.String</span></span>

## <span data-ttu-id="fdc48-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdc48-145">OUTPUTS</span></span>

### <span data-ttu-id="fdc48-146">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fdc48-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="fdc48-147">Note</span><span class="sxs-lookup"><span data-stu-id="fdc48-147">NOTES</span></span>

## <span data-ttu-id="fdc48-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdc48-148">RELATED LINKS</span></span>

[<span data-ttu-id="fdc48-149">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fdc48-149">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="fdc48-150">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fdc48-150">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="fdc48-151">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fdc48-151">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


