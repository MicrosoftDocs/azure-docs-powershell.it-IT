---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362641"
---
# <span data-ttu-id="99edb-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="99edb-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="99edb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99edb-102">SYNOPSIS</span></span>
<span data-ttu-id="99edb-103">Crea un oggetto di mapping del disco per i dischi della macchina virtuale vMWare da replicare.</span><span class="sxs-lookup"><span data-stu-id="99edb-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="99edb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99edb-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99edb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99edb-105">DESCRIPTION</span></span>
<span data-ttu-id="99edb-106">Crea un oggetto di mapping del disco che esegue il mapping di un disco di una macchina virtuale vMWare all'account di archiviazione della cache e al tipo di disco gestito di destinazione (area di ripristino) da usare per replicare il disco.</span><span class="sxs-lookup"><span data-stu-id="99edb-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="99edb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99edb-107">EXAMPLES</span></span>

### <span data-ttu-id="99edb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99edb-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="99edb-109">Creare un oggetto di mapping del disco per i dischi della macchina virtuale vMWare da replicare. Usato durante l'abilitazione della protezione per vMWare Machine.</span><span class="sxs-lookup"><span data-stu-id="99edb-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="99edb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99edb-110">PARAMETERS</span></span>

### <span data-ttu-id="99edb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99edb-111">-DefaultProfile</span></span>
<span data-ttu-id="99edb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99edb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99edb-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="99edb-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="99edb-114">Specifica l'ID risorsa del set di crittografia disco da usare per la crittografia dei dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="99edb-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99edb-115">-DiskID</span><span class="sxs-lookup"><span data-stu-id="99edb-115">-DiskId</span></span>
<span data-ttu-id="99edb-116">Specifica il DiskID del disco a cui corrisponde il mapping.</span><span class="sxs-lookup"><span data-stu-id="99edb-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="99edb-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="99edb-117">-DiskType</span></span>
<span data-ttu-id="99edb-118">Specifica il tipo di disco di ripristino.</span><span class="sxs-lookup"><span data-stu-id="99edb-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="99edb-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="99edb-119">-LogStorageAccountId</span></span>
<span data-ttu-id="99edb-120">Specifica l'ID dell'account di archiviazione del log o della cache da usare per archiviare i registri di replica.</span><span class="sxs-lookup"><span data-stu-id="99edb-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="99edb-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99edb-121">-Confirm</span></span>
<span data-ttu-id="99edb-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99edb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99edb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99edb-123">-WhatIf</span></span>
<span data-ttu-id="99edb-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99edb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99edb-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99edb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99edb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99edb-126">CommonParameters</span></span>
<span data-ttu-id="99edb-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99edb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99edb-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99edb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99edb-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99edb-129">INPUTS</span></span>

### <span data-ttu-id="99edb-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="99edb-130">None</span></span>

## <span data-ttu-id="99edb-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99edb-131">OUTPUTS</span></span>

### <span data-ttu-id="99edb-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="99edb-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="99edb-133">Note</span><span class="sxs-lookup"><span data-stu-id="99edb-133">NOTES</span></span>

## <span data-ttu-id="99edb-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99edb-134">RELATED LINKS</span></span>
