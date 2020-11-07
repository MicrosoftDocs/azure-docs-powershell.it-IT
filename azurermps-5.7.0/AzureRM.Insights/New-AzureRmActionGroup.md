---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: 9428ea3c297bcdab01ee6464d38b5c20910b69d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686106"
---
# <span data-ttu-id="e5a63-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="e5a63-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="e5a63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5a63-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a63-103">Crea un oggetto di riferimento ActionGroup in memoria.</span><span class="sxs-lookup"><span data-stu-id="e5a63-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5a63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5a63-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5a63-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5a63-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a63-106">Il cmdlet **New-AzureRmActionGroup** crea un oggetto di riferimento per il gruppo di azioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="e5a63-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="e5a63-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5a63-107">EXAMPLES</span></span>

### <span data-ttu-id="e5a63-108">Esempio 1: creare un oggetto di riferimento per il gruppo di azioni in memoria</span><span class="sxs-lookup"><span data-stu-id="e5a63-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="e5a63-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5a63-109">PARAMETERS</span></span>

### <span data-ttu-id="e5a63-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="e5a63-110">-ActionGroupId</span></span>
<span data-ttu-id="e5a63-111">ID/nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="e5a63-111">The Id/name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a63-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a63-112">-DefaultProfile</span></span>
<span data-ttu-id="e5a63-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e5a63-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5a63-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="e5a63-114">-WebhookProperty</span></span>
<span data-ttu-id="e5a63-115">Proprietà webhook del gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="e5a63-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="e5a63-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a63-116">CommonParameters</span></span>
<span data-ttu-id="e5a63-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a63-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a63-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5a63-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a63-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5a63-119">INPUTS</span></span>

### <span data-ttu-id="e5a63-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e5a63-120">None</span></span>
<span data-ttu-id="e5a63-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e5a63-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5a63-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5a63-122">OUTPUTS</span></span>

### <span data-ttu-id="e5a63-123">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="e5a63-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="e5a63-124">Note</span><span class="sxs-lookup"><span data-stu-id="e5a63-124">NOTES</span></span>

## <span data-ttu-id="e5a63-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5a63-125">RELATED LINKS</span></span>

[<span data-ttu-id="e5a63-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e5a63-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e5a63-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e5a63-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e5a63-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e5a63-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e5a63-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e5a63-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e5a63-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e5a63-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e5a63-131">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e5a63-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

