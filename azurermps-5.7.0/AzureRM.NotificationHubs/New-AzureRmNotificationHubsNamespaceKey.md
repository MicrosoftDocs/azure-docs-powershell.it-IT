---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 4756402ab46deb0260db19474a26e2c568055187
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521010"
---
# <span data-ttu-id="36e6d-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="36e6d-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="36e6d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="36e6d-103">Rigenerare la chiave della regola di autorizzazione per uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="36e6d-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36e6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36e6d-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36e6d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="36e6d-106">New-AzureRmNotificationHubNamespaceKey cmdlet rigenera la chiave primaria/secondaria per la regola di autorizzazione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="36e6d-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="36e6d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36e6d-107">EXAMPLES</span></span>

### <span data-ttu-id="36e6d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="36e6d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="36e6d-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="36e6d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="36e6d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36e6d-110">PARAMETERS</span></span>

### <span data-ttu-id="36e6d-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36e6d-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e6d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e6d-112">-DefaultProfile</span></span>
<span data-ttu-id="36e6d-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="36e6d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e6d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="36e6d-114">-Force</span></span>
<span data-ttu-id="36e6d-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="36e6d-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e6d-116">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="36e6d-116">-Namespace</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e6d-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="36e6d-117">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e6d-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36e6d-118">-ResourceGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36e6d-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36e6d-119">-Confirm</span></span>
<span data-ttu-id="36e6d-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36e6d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e6d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e6d-121">-WhatIf</span></span>
<span data-ttu-id="36e6d-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36e6d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e6d-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36e6d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e6d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e6d-124">CommonParameters</span></span>
<span data-ttu-id="36e6d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e6d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e6d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36e6d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e6d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36e6d-127">INPUTS</span></span>

### <span data-ttu-id="36e6d-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="36e6d-128">None</span></span>
<span data-ttu-id="36e6d-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="36e6d-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36e6d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36e6d-130">OUTPUTS</span></span>

### <span data-ttu-id="36e6d-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="36e6d-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="36e6d-132">Note</span><span class="sxs-lookup"><span data-stu-id="36e6d-132">NOTES</span></span>

## <span data-ttu-id="36e6d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36e6d-133">RELATED LINKS</span></span>

