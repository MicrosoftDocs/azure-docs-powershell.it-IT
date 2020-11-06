---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: c5d86909bffa7c38d66c31b56b34a66251b21d65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507352"
---
# <span data-ttu-id="3b3a7-101">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3b3a7-101">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="3b3a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3a7-103">Aggiungere (individuare) un server fisico all'elenco degli elementi protettivi.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-103">Add(Discover) a physical server to the list of protectable items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b3a7-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 -FriendlyName <String> -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b3a7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b3a7-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3a7-106">Il **nuovo AzureRmRecoveryServicesAsrProtectableItem** aggiunge un nuovo elemento protettivo all'elenco degli elementi protettivi individuati in un contenitore di protezione all'interno di un tessuto ASR (applicabile solo per il tipo di tessuto VMware).</span><span class="sxs-lookup"><span data-stu-id="3b3a7-106">The **New-AzureRmRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="3b3a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b3a7-107">EXAMPLES</span></span>

### <span data-ttu-id="3b3a7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3b3a7-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="3b3a7-109">Aggiungere o individuare il nuovo servizio di recupero di Azure ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="3b3a7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b3a7-110">PARAMETERS</span></span>

### <span data-ttu-id="3b3a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3a7-111">-DefaultProfile</span></span>
<span data-ttu-id="3b3a7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b3a7-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3b3a7-113">-FriendlyName</span></span>
<span data-ttu-id="3b3a7-114">Nome descrittivo per l'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-114">Friendly name for the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a7-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="3b3a7-115">-IPAddress</span></span>
<span data-ttu-id="3b3a7-116">Indirizzo IP dell'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-116">IP address of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a7-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="3b3a7-117">-OSType</span></span>
<span data-ttu-id="3b3a7-118">Tipo di sistema operativo (Windows/Linux) dell'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a7-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3b3a7-119">-ProtectionContainer</span></span>
<span data-ttu-id="3b3a7-120">Oggetto contenitore di protezione ASR a cui deve essere aggiunto l'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-120">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a7-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b3a7-121">-Confirm</span></span>
<span data-ttu-id="3b3a7-122">Richiedi conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b3a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3a7-123">-WhatIf</span></span>
<span data-ttu-id="3b3a7-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b3a7-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b3a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3a7-126">CommonParameters</span></span>
<span data-ttu-id="3b3a7-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3a7-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3a7-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b3a7-129">INPUTS</span></span>

### <span data-ttu-id="3b3a7-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3b3a7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="3b3a7-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b3a7-131">OUTPUTS</span></span>

### <span data-ttu-id="3b3a7-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3b3a7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3b3a7-133">Note</span><span class="sxs-lookup"><span data-stu-id="3b3a7-133">NOTES</span></span>

## <span data-ttu-id="3b3a7-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b3a7-134">RELATED LINKS</span></span>
