---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: b2f9738518f446b9cf5bfbefe0c7025bb3351628
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865830"
---
# <span data-ttu-id="71d83-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="71d83-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="71d83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71d83-102">SYNOPSIS</span></span>
<span data-ttu-id="71d83-103">Crea un oggetto di riferimento ActionGroup in memoria.</span><span class="sxs-lookup"><span data-stu-id="71d83-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71d83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71d83-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71d83-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71d83-105">DESCRIPTION</span></span>
<span data-ttu-id="71d83-106">Il cmdlet **New-AzureRmActionGroup** crea un oggetto di riferimento per il gruppo di azioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="71d83-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="71d83-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71d83-107">EXAMPLES</span></span>

### <span data-ttu-id="71d83-108">Esempio 1: creare un oggetto di riferimento per il gruppo di azioni in memoria</span><span class="sxs-lookup"><span data-stu-id="71d83-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="71d83-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71d83-109">PARAMETERS</span></span>

### <span data-ttu-id="71d83-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="71d83-110">-ActionGroupId</span></span>
<span data-ttu-id="71d83-111">ID/nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="71d83-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="71d83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71d83-112">-DefaultProfile</span></span>
<span data-ttu-id="71d83-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="71d83-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71d83-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="71d83-114">-WebhookProperty</span></span>
<span data-ttu-id="71d83-115">Proprietà webhook del gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="71d83-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="71d83-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71d83-116">CommonParameters</span></span>
<span data-ttu-id="71d83-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71d83-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71d83-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71d83-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71d83-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71d83-119">INPUTS</span></span>

### <span data-ttu-id="71d83-120">System. String</span><span class="sxs-lookup"><span data-stu-id="71d83-120">System.String</span></span>

### <span data-ttu-id="71d83-121">System. Collections. Generic. Dictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="71d83-121">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="71d83-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71d83-122">OUTPUTS</span></span>

### <span data-ttu-id="71d83-123">Microsoft. Azure. Management. monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="71d83-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="71d83-124">Note</span><span class="sxs-lookup"><span data-stu-id="71d83-124">NOTES</span></span>

## <span data-ttu-id="71d83-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71d83-125">RELATED LINKS</span></span>

[<span data-ttu-id="71d83-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71d83-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="71d83-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71d83-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="71d83-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71d83-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="71d83-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71d83-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="71d83-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71d83-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="71d83-131">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="71d83-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

