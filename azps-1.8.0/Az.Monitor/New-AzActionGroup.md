---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 6fd3ceb5a0c49b5c8b4f530deddb31fdf5b09f4a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403086"
---
# <span data-ttu-id="4b16e-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="4b16e-101">New-AzActionGroup</span></span>

## <span data-ttu-id="4b16e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b16e-102">SYNOPSIS</span></span>
<span data-ttu-id="4b16e-103">Crea un oggetto riferimento ActionGroup in memoria.</span><span class="sxs-lookup"><span data-stu-id="4b16e-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="4b16e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b16e-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b16e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4b16e-105">DESCRIPTION</span></span>
<span data-ttu-id="4b16e-106">Il cmdlet **New-AzActionGroup** crea un oggetto riferimento al gruppo di azioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="4b16e-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="4b16e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b16e-107">EXAMPLES</span></span>

### <span data-ttu-id="4b16e-108">Esempio 1: Creare un oggetto riferimento a un gruppo di azioni in memoria</span><span class="sxs-lookup"><span data-stu-id="4b16e-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="4b16e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b16e-109">PARAMETERS</span></span>

### <span data-ttu-id="4b16e-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="4b16e-110">-ActionGroupId</span></span>
<span data-ttu-id="4b16e-111">ID/nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="4b16e-111">The Id/name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b16e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b16e-112">-DefaultProfile</span></span>
<span data-ttu-id="4b16e-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4b16e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b16e-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="4b16e-114">-WebhookProperty</span></span>
<span data-ttu-id="4b16e-115">Proprietà Webhook del gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="4b16e-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b16e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b16e-116">CommonParameters</span></span>
<span data-ttu-id="4b16e-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b16e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b16e-118">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b16e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b16e-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="4b16e-119">INPUTS</span></span>

### <span data-ttu-id="4b16e-120">System.String</span><span class="sxs-lookup"><span data-stu-id="4b16e-120">System.String</span></span>

### <span data-ttu-id="4b16e-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b16e-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4b16e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b16e-122">OUTPUTS</span></span>

### <span data-ttu-id="4b16e-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="4b16e-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="4b16e-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="4b16e-124">NOTES</span></span>

## <span data-ttu-id="4b16e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b16e-125">RELATED LINKS</span></span>

[<span data-ttu-id="4b16e-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4b16e-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="4b16e-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4b16e-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="4b16e-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4b16e-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="4b16e-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4b16e-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="4b16e-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4b16e-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)



