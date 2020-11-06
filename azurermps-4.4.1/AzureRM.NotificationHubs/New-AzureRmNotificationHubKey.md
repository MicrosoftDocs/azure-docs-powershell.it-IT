---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: 419dd6efcf9152c03d3f94f5ab9ead06c3c234ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516172"
---
# <span data-ttu-id="9a2a0-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="9a2a0-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="9a2a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="9a2a0-103">Rigenerare la chiave della regola di autorizzazione per un NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="9a2a0-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a2a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a2a0-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a2a0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a2a0-105">DESCRIPTION</span></span>
<span data-ttu-id="9a2a0-106">New-AzureRmNotificationHubKey cmdlet rigenera la chiave primaria/secondaria per la regola di autorizzazione NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="9a2a0-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="9a2a0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a2a0-107">EXAMPLES</span></span>

### <span data-ttu-id="9a2a0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a2a0-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9a2a0-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="9a2a0-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9a2a0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a2a0-110">PARAMETERS</span></span>

### <span data-ttu-id="9a2a0-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9a2a0-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="9a2a0-112">-Force</span><span class="sxs-lookup"><span data-stu-id="9a2a0-112">-Force</span></span>
<span data-ttu-id="9a2a0-113">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9a2a0-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9a2a0-114">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9a2a0-114">-Namespace</span></span>
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

### <span data-ttu-id="9a2a0-115">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="9a2a0-115">-NotificationHub</span></span>
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

### <span data-ttu-id="9a2a0-116">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="9a2a0-116">-PolicyKey</span></span>
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

### <span data-ttu-id="9a2a0-117">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9a2a0-117">-ResourceGroup</span></span>
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

### <span data-ttu-id="9a2a0-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9a2a0-118">-Confirm</span></span>
<span data-ttu-id="9a2a0-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a2a0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a2a0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a2a0-120">-WhatIf</span></span>
<span data-ttu-id="9a2a0-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a2a0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a2a0-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a2a0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a2a0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a2a0-123">-DefaultProfile</span></span>
<span data-ttu-id="9a2a0-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a2a0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a2a0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a2a0-125">CommonParameters</span></span>
<span data-ttu-id="9a2a0-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a2a0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a2a0-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a2a0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a2a0-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a2a0-128">INPUTS</span></span>

## <span data-ttu-id="9a2a0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a2a0-129">OUTPUTS</span></span>

### <span data-ttu-id="9a2a0-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="9a2a0-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="9a2a0-131">Note</span><span class="sxs-lookup"><span data-stu-id="9a2a0-131">NOTES</span></span>

## <span data-ttu-id="9a2a0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a2a0-132">RELATED LINKS</span></span>

