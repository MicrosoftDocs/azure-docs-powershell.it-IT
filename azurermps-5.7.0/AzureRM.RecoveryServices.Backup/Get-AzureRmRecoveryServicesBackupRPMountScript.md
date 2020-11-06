---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 0f3f0292b4f348207bf80d5e04c63dc45be69fa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509747"
---
# <span data-ttu-id="a40d4-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="a40d4-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="a40d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a40d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a40d4-103">Scarica uno script per montare tutti i file del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a40d4-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a40d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a40d4-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a40d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a40d4-105">DESCRIPTION</span></span>
<span data-ttu-id="a40d4-106">Il cmdlet Get-AzureRmRecoveryServicesBackupRPMountScript Scarica uno script che monta i volumi del punto di recupero nel computer in cui viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a40d4-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="a40d4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a40d4-107">EXAMPLES</span></span>

### <span data-ttu-id="a40d4-108">Esempio 1: montare un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="a40d4-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="a40d4-109">Quando lo script viene eseguito, verranno montati i file del punto di ripristino $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="a40d4-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="a40d4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a40d4-110">PARAMETERS</span></span>

### <span data-ttu-id="a40d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40d4-111">-DefaultProfile</span></span>
<span data-ttu-id="a40d4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a40d4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a40d4-113">-Path</span><span class="sxs-lookup"><span data-stu-id="a40d4-113">-Path</span></span>
<span data-ttu-id="a40d4-114">Posizione in cui il file deve essere scaricato in caso di recupero file.</span><span class="sxs-lookup"><span data-stu-id="a40d4-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="a40d4-115">Se-path non è disponibile, il file di script verrà scaricato nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="a40d4-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40d4-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a40d4-116">-RecoveryPoint</span></span>
<span data-ttu-id="a40d4-117">Oggetto punto di ripristino da ripristinare</span><span class="sxs-lookup"><span data-stu-id="a40d4-117">Recovery point object to be restored</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a40d4-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a40d4-118">-Confirm</span></span>
<span data-ttu-id="a40d4-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a40d4-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40d4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a40d4-120">-WhatIf</span></span>
<span data-ttu-id="a40d4-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a40d4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a40d4-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a40d4-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40d4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40d4-123">CommonParameters</span></span>
<span data-ttu-id="a40d4-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40d4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40d4-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40d4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40d4-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a40d4-126">INPUTS</span></span>

### <span data-ttu-id="a40d4-127">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="a40d4-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="a40d4-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a40d4-128">OUTPUTS</span></span>

### <span data-ttu-id="a40d4-129">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="a40d4-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="a40d4-130">Note</span><span class="sxs-lookup"><span data-stu-id="a40d4-130">NOTES</span></span>

## <span data-ttu-id="a40d4-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a40d4-131">RELATED LINKS</span></span>

