---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: b6782eccb7a27204cffe91d8cb858b23f8e94f5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521370"
---
# <span data-ttu-id="b59a5-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b59a5-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="b59a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b59a5-102">SYNOPSIS</span></span>
<span data-ttu-id="b59a5-103">Crea un oggetto di riferimento ActionGroup in memoria.</span><span class="sxs-lookup"><span data-stu-id="b59a5-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b59a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b59a5-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b59a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b59a5-105">DESCRIPTION</span></span>
<span data-ttu-id="b59a5-106">Il cmdlet **New-AzureRmActionGroup** crea un oggetto di riferimento per il gruppo di azioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="b59a5-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="b59a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b59a5-107">EXAMPLES</span></span>

### <span data-ttu-id="b59a5-108">Esempio 1: creare un oggetto di riferimento per il gruppo di azioni in memoria</span><span class="sxs-lookup"><span data-stu-id="b59a5-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="b59a5-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b59a5-109">PARAMETERS</span></span>

### <span data-ttu-id="b59a5-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="b59a5-110">-ActionGroupId</span></span>
<span data-ttu-id="b59a5-111">ID/nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="b59a5-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="b59a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59a5-112">-DefaultProfile</span></span>
<span data-ttu-id="b59a5-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b59a5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b59a5-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="b59a5-114">-WebhookProperty</span></span>
<span data-ttu-id="b59a5-115">Proprietà webhook del gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="b59a5-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="b59a5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59a5-116">CommonParameters</span></span>
<span data-ttu-id="b59a5-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b59a5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59a5-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b59a5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59a5-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b59a5-119">INPUTS</span></span>

### <span data-ttu-id="b59a5-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b59a5-120">System.String</span></span>

### <span data-ttu-id="b59a5-121">System. Collections. Generic. Dictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b59a5-121">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b59a5-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b59a5-122">OUTPUTS</span></span>

### <span data-ttu-id="b59a5-123">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="b59a5-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="b59a5-124">Note</span><span class="sxs-lookup"><span data-stu-id="b59a5-124">NOTES</span></span>

## <span data-ttu-id="b59a5-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b59a5-125">RELATED LINKS</span></span>

[<span data-ttu-id="b59a5-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b59a5-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b59a5-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b59a5-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b59a5-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b59a5-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b59a5-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b59a5-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b59a5-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b59a5-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b59a5-131">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="b59a5-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

