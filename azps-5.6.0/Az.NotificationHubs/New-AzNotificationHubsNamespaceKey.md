---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: 2d3fb02aa41d58521d35382aa35eb47c4b1d523c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951165"
---
# <span data-ttu-id="034ee-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="034ee-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="034ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="034ee-102">SYNOPSIS</span></span>
<span data-ttu-id="034ee-103">Rigenerare la chiave della regola di autorizzazione per uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="034ee-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="034ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="034ee-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="034ee-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="034ee-105">DESCRIPTION</span></span>
<span data-ttu-id="034ee-106">New-AzNotificationHubNamespaceKey cmdlet rigenera la chiave primaria/chiave secondaria per la regola di autorizzazione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="034ee-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="034ee-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="034ee-107">EXAMPLES</span></span>

### <span data-ttu-id="034ee-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="034ee-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="034ee-109">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="034ee-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="034ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="034ee-110">PARAMETERS</span></span>

### <span data-ttu-id="034ee-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="034ee-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="034ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034ee-112">-DefaultProfile</span></span>
<span data-ttu-id="034ee-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="034ee-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="034ee-114">-Force</span><span class="sxs-lookup"><span data-stu-id="034ee-114">-Force</span></span>
<span data-ttu-id="034ee-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="034ee-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="034ee-116">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="034ee-116">-Namespace</span></span>
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

### <span data-ttu-id="034ee-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="034ee-117">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034ee-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="034ee-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="034ee-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="034ee-119">-Confirm</span></span>
<span data-ttu-id="034ee-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="034ee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="034ee-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="034ee-121">-WhatIf</span></span>
<span data-ttu-id="034ee-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="034ee-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="034ee-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="034ee-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="034ee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034ee-124">CommonParameters</span></span>
<span data-ttu-id="034ee-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="034ee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034ee-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="034ee-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034ee-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="034ee-127">INPUTS</span></span>

### <span data-ttu-id="034ee-128">System.String</span><span class="sxs-lookup"><span data-stu-id="034ee-128">System.String</span></span>

## <span data-ttu-id="034ee-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="034ee-129">OUTPUTS</span></span>

### <span data-ttu-id="034ee-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="034ee-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="034ee-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="034ee-131">NOTES</span></span>

## <span data-ttu-id="034ee-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="034ee-132">RELATED LINKS</span></span>
