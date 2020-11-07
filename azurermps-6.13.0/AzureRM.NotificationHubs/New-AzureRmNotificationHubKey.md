---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: d129d34ab9bcbcd67a7c643e4f412bacf262b293
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521316"
---
# <span data-ttu-id="2b6e3-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="2b6e3-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="2b6e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b6e3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6e3-103">Rigenerare la chiave della regola di autorizzazione per un NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="2b6e3-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b6e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b6e3-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b6e3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b6e3-105">DESCRIPTION</span></span>
<span data-ttu-id="2b6e3-106">New-AzureRmNotificationHubKey cmdlet rigenera la chiave primaria/secondaria per la regola di autorizzazione NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="2b6e3-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="2b6e3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b6e3-107">EXAMPLES</span></span>

### <span data-ttu-id="2b6e3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b6e3-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2b6e3-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="2b6e3-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="2b6e3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b6e3-110">PARAMETERS</span></span>

### <span data-ttu-id="2b6e3-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2b6e3-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6e3-112">-DefaultProfile</span></span>
<span data-ttu-id="2b6e3-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2b6e3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b6e3-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2b6e3-114">-Force</span></span>
<span data-ttu-id="2b6e3-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2b6e3-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e3-116">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2b6e3-116">-Namespace</span></span>
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

### <span data-ttu-id="2b6e3-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="2b6e3-117">-NotificationHub</span></span>
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

### <span data-ttu-id="2b6e3-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="2b6e3-118">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6e3-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b6e3-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="2b6e3-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b6e3-120">-Confirm</span></span>
<span data-ttu-id="2b6e3-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b6e3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b6e3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b6e3-122">-WhatIf</span></span>
<span data-ttu-id="2b6e3-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b6e3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b6e3-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b6e3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b6e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6e3-125">CommonParameters</span></span>
<span data-ttu-id="2b6e3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b6e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6e3-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6e3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6e3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b6e3-128">INPUTS</span></span>

### <span data-ttu-id="2b6e3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2b6e3-129">System.String</span></span>

## <span data-ttu-id="2b6e3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b6e3-130">OUTPUTS</span></span>

### <span data-ttu-id="2b6e3-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="2b6e3-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="2b6e3-132">Note</span><span class="sxs-lookup"><span data-stu-id="2b6e3-132">NOTES</span></span>

## <span data-ttu-id="2b6e3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b6e3-133">RELATED LINKS</span></span>