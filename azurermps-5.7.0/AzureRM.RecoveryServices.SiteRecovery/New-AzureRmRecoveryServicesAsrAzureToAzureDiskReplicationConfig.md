---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508071"
---
# <span data-ttu-id="4d80b-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="4d80b-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="4d80b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d80b-102">SYNOPSIS</span></span>
<span data-ttu-id="4d80b-103">Crea un oggetto di mapping del disco per i dischi di una macchina virtuale Azure da replicare.</span><span class="sxs-lookup"><span data-stu-id="4d80b-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d80b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d80b-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d80b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d80b-105">DESCRIPTION</span></span>
<span data-ttu-id="4d80b-106">Crea un oggetto di mapping del disco che esegue il mapping di un disco di una macchina virtuale di Azure all'account di archiviazione della cache e dell'account di archiviazione di destinazione (area di ripristino) da usare per replicare il disco.</span><span class="sxs-lookup"><span data-stu-id="4d80b-106">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="4d80b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d80b-107">EXAMPLES</span></span>

### <span data-ttu-id="4d80b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d80b-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="4d80b-109">Creare un oggetto di mapping del disco per i dischi di una macchina virtuale di Azure da replicare. Usato durante Azure in Azure per abilitare e proteggere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4d80b-109">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="4d80b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d80b-110">PARAMETERS</span></span>

### <span data-ttu-id="4d80b-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d80b-111">-Confirm</span></span>
<span data-ttu-id="4d80b-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d80b-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d80b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d80b-113">-DefaultProfile</span></span>
<span data-ttu-id="4d80b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d80b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d80b-115">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4d80b-115">-LogStorageAccountId</span></span>
<span data-ttu-id="4d80b-116">Specifica l'ID dell'account di archiviazione del log o della cache da usare per archiviare i registri di replica.</span><span class="sxs-lookup"><span data-stu-id="4d80b-116">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="4d80b-117">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4d80b-117">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="4d80b-118">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="4d80b-118">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="4d80b-119">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="4d80b-119">-VhdUri</span></span>
<span data-ttu-id="4d80b-120">Specifica l'URI VHD del disco a cui corrisponde il mapping.</span><span class="sxs-lookup"><span data-stu-id="4d80b-120">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="4d80b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d80b-121">-WhatIf</span></span>
<span data-ttu-id="4d80b-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d80b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d80b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d80b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d80b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d80b-124">CommonParameters</span></span>
<span data-ttu-id="4d80b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d80b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d80b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d80b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d80b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d80b-127">INPUTS</span></span>

### <span data-ttu-id="4d80b-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4d80b-128">None</span></span>

## <span data-ttu-id="4d80b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d80b-129">OUTPUTS</span></span>

### <span data-ttu-id="4d80b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="4d80b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="4d80b-131">Note</span><span class="sxs-lookup"><span data-stu-id="4d80b-131">NOTES</span></span>

## <span data-ttu-id="4d80b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d80b-132">RELATED LINKS</span></span>
