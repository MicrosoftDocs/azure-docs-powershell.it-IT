---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 8973c3606c7c29c254650b3412275c1dfd7bf761
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520414"
---
# <span data-ttu-id="c41e0-101">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c41e0-101">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="c41e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c41e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c41e0-103">Aggiungere (individuare) un server fisico all'elenco degli elementi protettivi.</span><span class="sxs-lookup"><span data-stu-id="c41e0-103">Add(Discover) a physical server to the list of protectable items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c41e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c41e0-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 -FriendlyName <String> -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c41e0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c41e0-105">DESCRIPTION</span></span>
<span data-ttu-id="c41e0-106">Il **nuovo AzureRmRecoveryServicesAsrProtectableItem** aggiunge un nuovo elemento protettivo all'elenco degli elementi protettivi individuati in un contenitore di protezione all'interno di un tessuto ASR (applicabile solo per il tipo di tessuto VMware).</span><span class="sxs-lookup"><span data-stu-id="c41e0-106">The **New-AzureRmRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="c41e0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c41e0-107">EXAMPLES</span></span>

### <span data-ttu-id="c41e0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c41e0-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectableItem ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="c41e0-109">Aggiungere o individuare il nuovo servizio di recupero di Azure ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="c41e0-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="c41e0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c41e0-110">PARAMETERS</span></span>

### <span data-ttu-id="c41e0-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c41e0-111">-Confirm</span></span>
<span data-ttu-id="c41e0-112">Richiedi conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c41e0-112">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c41e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c41e0-113">-DefaultProfile</span></span>
<span data-ttu-id="c41e0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c41e0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c41e0-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c41e0-115">-FriendlyName</span></span>
<span data-ttu-id="c41e0-116">Nome descrittivo per l'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="c41e0-116">Friendly name for the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c41e0-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="c41e0-117">-IPAddress</span></span>
<span data-ttu-id="c41e0-118">Indirizzo IP dell'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="c41e0-118">IP address of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c41e0-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="c41e0-119">-OSType</span></span>
<span data-ttu-id="c41e0-120">Tipo di sistema operativo (Windows/Linux) dell'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="c41e0-120">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c41e0-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c41e0-121">-ProtectionContainer</span></span>
<span data-ttu-id="c41e0-122">Oggetto contenitore di protezione ASR a cui deve essere aggiunto l'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="c41e0-122">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c41e0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c41e0-123">-WhatIf</span></span>
<span data-ttu-id="c41e0-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c41e0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c41e0-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c41e0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c41e0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41e0-126">CommonParameters</span></span>
<span data-ttu-id="c41e0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c41e0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41e0-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c41e0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41e0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c41e0-129">INPUTS</span></span>

### <span data-ttu-id="c41e0-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c41e0-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="c41e0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c41e0-131">OUTPUTS</span></span>

### <span data-ttu-id="c41e0-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c41e0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c41e0-133">Note</span><span class="sxs-lookup"><span data-stu-id="c41e0-133">NOTES</span></span>

## <span data-ttu-id="c41e0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c41e0-134">RELATED LINKS</span></span>
