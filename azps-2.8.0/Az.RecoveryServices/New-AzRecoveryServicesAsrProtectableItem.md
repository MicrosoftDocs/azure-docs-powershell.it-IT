---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 57f9009ead66eb87685aaf0142c6dbd8b125f307
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855653"
---
# <span data-ttu-id="0086e-101">New-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0086e-101">New-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="0086e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0086e-102">SYNOPSIS</span></span>
<span data-ttu-id="0086e-103">Aggiungere (individuare) un server fisico all'elenco degli elementi protettivi.</span><span class="sxs-lookup"><span data-stu-id="0086e-103">Add(Discover) a physical server to the list of protectable items.</span></span>

## <span data-ttu-id="0086e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0086e-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer> -FriendlyName <String>
 -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0086e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0086e-105">DESCRIPTION</span></span>
<span data-ttu-id="0086e-106">Il **nuovo AzRecoveryServicesAsrProtectableItem** aggiunge un nuovo elemento protettivo all'elenco degli elementi protettivi individuati in un contenitore di protezione all'interno di un tessuto ASR (applicabile solo per il tipo di tessuto VMware).</span><span class="sxs-lookup"><span data-stu-id="0086e-106">The **New-AzRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="0086e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0086e-107">EXAMPLES</span></span>

### <span data-ttu-id="0086e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0086e-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="0086e-109">Aggiungere o individuare il nuovo servizio di recupero di Azure ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="0086e-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="0086e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0086e-110">PARAMETERS</span></span>

### <span data-ttu-id="0086e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0086e-111">-DefaultProfile</span></span>
<span data-ttu-id="0086e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0086e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0086e-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0086e-113">-FriendlyName</span></span>
<span data-ttu-id="0086e-114">Nome descrittivo per l'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="0086e-114">Friendly name for the protectable item.</span></span>

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

### <span data-ttu-id="0086e-115">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="0086e-115">-IPAddress</span></span>
<span data-ttu-id="0086e-116">Indirizzo IP dell'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="0086e-116">IP address of the protectable item.</span></span>

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

### <span data-ttu-id="0086e-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="0086e-117">-OSType</span></span>
<span data-ttu-id="0086e-118">Tipo di sistema operativo (Windows/Linux) dell'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="0086e-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

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

### <span data-ttu-id="0086e-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0086e-119">-ProtectionContainer</span></span>
<span data-ttu-id="0086e-120">Oggetto contenitore di protezione ASR a cui deve essere aggiunto l'elemento protettivo.</span><span class="sxs-lookup"><span data-stu-id="0086e-120">ASR Protection container object to which the protectable item should be added.</span></span>

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

### <span data-ttu-id="0086e-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0086e-121">-Confirm</span></span>
<span data-ttu-id="0086e-122">Richiedi conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0086e-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0086e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0086e-123">-WhatIf</span></span>
<span data-ttu-id="0086e-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0086e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0086e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0086e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0086e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0086e-126">CommonParameters</span></span>
<span data-ttu-id="0086e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0086e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0086e-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0086e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0086e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0086e-129">INPUTS</span></span>

### <span data-ttu-id="0086e-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0086e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="0086e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0086e-131">OUTPUTS</span></span>

### <span data-ttu-id="0086e-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0086e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0086e-133">Note</span><span class="sxs-lookup"><span data-stu-id="0086e-133">NOTES</span></span>

## <span data-ttu-id="0086e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0086e-134">RELATED LINKS</span></span>
