---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: 01ba4388d1cb6166c927096144e628d9fc2d81a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855558"
---
# <span data-ttu-id="cb603-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="cb603-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="cb603-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb603-102">SYNOPSIS</span></span>
<span data-ttu-id="cb603-103">Rigenerare la chiave della regola di autorizzazione per uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cb603-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="cb603-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb603-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb603-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb603-105">DESCRIPTION</span></span>
<span data-ttu-id="cb603-106">New-AzNotificationHubNamespaceKey cmdlet rigenera la chiave primaria/secondaria per la regola di autorizzazione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cb603-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="cb603-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb603-107">EXAMPLES</span></span>

### <span data-ttu-id="cb603-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cb603-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="cb603-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="cb603-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="cb603-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb603-110">PARAMETERS</span></span>

### <span data-ttu-id="cb603-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb603-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="cb603-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb603-112">-DefaultProfile</span></span>
<span data-ttu-id="cb603-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cb603-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb603-114">-Force</span><span class="sxs-lookup"><span data-stu-id="cb603-114">-Force</span></span>
<span data-ttu-id="cb603-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cb603-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cb603-116">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cb603-116">-Namespace</span></span>
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

### <span data-ttu-id="cb603-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="cb603-117">-PolicyKey</span></span>
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

### <span data-ttu-id="cb603-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cb603-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="cb603-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cb603-119">-Confirm</span></span>
<span data-ttu-id="cb603-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb603-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb603-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb603-121">-WhatIf</span></span>
<span data-ttu-id="cb603-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb603-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb603-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb603-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb603-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb603-124">CommonParameters</span></span>
<span data-ttu-id="cb603-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb603-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb603-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb603-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb603-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb603-127">INPUTS</span></span>

### <span data-ttu-id="cb603-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cb603-128">System.String</span></span>

## <span data-ttu-id="cb603-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb603-129">OUTPUTS</span></span>

### <span data-ttu-id="cb603-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="cb603-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="cb603-131">Note</span><span class="sxs-lookup"><span data-stu-id="cb603-131">NOTES</span></span>

## <span data-ttu-id="cb603-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb603-132">RELATED LINKS</span></span>
