---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192878"
---
# <span data-ttu-id="b7d79-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="b7d79-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="b7d79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7d79-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d79-103">Crea un oggetto di mapping del disco per i dischi delle macchine virtuali vMWare da replicare.</span><span class="sxs-lookup"><span data-stu-id="b7d79-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="b7d79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7d79-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7d79-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b7d79-105">DESCRIPTION</span></span>
<span data-ttu-id="b7d79-106">Crea un oggetto di mapping del disco che esegue il mapping di un disco della macchina virtuale vMWare all'account di archiviazione cache e al tipo di disco gestito di destinazione (area di ripristino) da usare per replicare il disco.</span><span class="sxs-lookup"><span data-stu-id="b7d79-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="b7d79-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7d79-107">EXAMPLES</span></span>

### <span data-ttu-id="b7d79-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b7d79-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="b7d79-109">Creare un oggetto di mapping del disco per i dischi delle macchine virtuali vMWare da replicare. Usato durante l'abilitazione della protezione per computer vMWare.</span><span class="sxs-lookup"><span data-stu-id="b7d79-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="b7d79-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7d79-110">PARAMETERS</span></span>

### <span data-ttu-id="b7d79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d79-111">-DefaultProfile</span></span>
<span data-ttu-id="b7d79-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7d79-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7d79-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b7d79-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b7d79-114">Specifica l'ID risorsa del set di crittografia del disco da usare per la crittografia dei dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="b7d79-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="b7d79-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="b7d79-115">-DiskId</span></span>
<span data-ttu-id="b7d79-116">Specificare l'ID Disco del disco a cui corrisponde questo mapping.</span><span class="sxs-lookup"><span data-stu-id="b7d79-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="b7d79-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="b7d79-117">-DiskType</span></span>
<span data-ttu-id="b7d79-118">Specifica il tipo di disco di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b7d79-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="b7d79-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b7d79-119">-LogStorageAccountId</span></span>
<span data-ttu-id="b7d79-120">Specifica l'ID dell'account di archiviazione cache o del log da usare per archiviare i log di replica.</span><span class="sxs-lookup"><span data-stu-id="b7d79-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="b7d79-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7d79-121">-Confirm</span></span>
<span data-ttu-id="b7d79-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7d79-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7d79-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7d79-123">-WhatIf</span></span>
<span data-ttu-id="b7d79-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7d79-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7d79-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7d79-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7d79-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d79-126">CommonParameters</span></span>
<span data-ttu-id="b7d79-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7d79-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d79-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7d79-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d79-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="b7d79-129">INPUTS</span></span>

### <span data-ttu-id="b7d79-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b7d79-130">None</span></span>

## <span data-ttu-id="b7d79-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7d79-131">OUTPUTS</span></span>

### <span data-ttu-id="b7d79-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="b7d79-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="b7d79-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="b7d79-133">NOTES</span></span>

## <span data-ttu-id="b7d79-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7d79-134">RELATED LINKS</span></span>
