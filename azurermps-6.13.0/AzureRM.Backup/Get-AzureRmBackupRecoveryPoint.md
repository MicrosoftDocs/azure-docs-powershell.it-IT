---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: f82abc45a9b78093c13764ab0eb28f2593c7fabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517628"
---
# <span data-ttu-id="d096b-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d096b-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="d096b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d096b-102">SYNOPSIS</span></span>
<span data-ttu-id="d096b-103">Ottiene i punti di ripristino per un elemento di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="d096b-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d096b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d096b-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d096b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d096b-105">DESCRIPTION</span></span>
<span data-ttu-id="d096b-106">Il cmdlet **Get-AzureRmBackupRecoveryPoint** ottiene i punti di ripristino per un elemento di backup di Azure supportato.</span><span class="sxs-lookup"><span data-stu-id="d096b-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="d096b-107">Dopo aver eseguito il backup di un elemento, il backup archivia uno o più punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d096b-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="d096b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d096b-108">EXAMPLES</span></span>

### <span data-ttu-id="d096b-109">Esempio 1: ottenere punti di ripristino per un elemento</span><span class="sxs-lookup"><span data-stu-id="d096b-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="d096b-110">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="d096b-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="d096b-111">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="d096b-111">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="d096b-112">Il secondo comando ottiene un contenitore con il nome specificato nel Vault in $Vault usando il cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="d096b-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="d096b-113">Il comando Archivia l'oggetto nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="d096b-113">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="d096b-114">Il terzo comando ottiene l'elemento di backup nel contenitore in $Container usando il cmdlet **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="d096b-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="d096b-115">Il comando Archivia l'oggetto nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d096b-115">The command stores that object in the $BackupItem variable.</span></span>
<span data-ttu-id="d096b-116">Il comando finale ottiene i punti di ripristino per l'elemento in $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d096b-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="d096b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d096b-117">PARAMETERS</span></span>

### <span data-ttu-id="d096b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d096b-118">-DefaultProfile</span></span>
<span data-ttu-id="d096b-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d096b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d096b-120">-Elemento</span><span class="sxs-lookup"><span data-stu-id="d096b-120">-Item</span></span>
<span data-ttu-id="d096b-121">Specifica l'elemento per cui questo cmdlet ottiene i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d096b-121">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="d096b-122">Per ottenere un **AzureRmBackupItem** , usare il cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="d096b-122">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d096b-123">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="d096b-123">-RecoveryPointId</span></span>
<span data-ttu-id="d096b-124">Specifica l'ID di un punto di recupero ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d096b-124">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d096b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d096b-125">CommonParameters</span></span>
<span data-ttu-id="d096b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d096b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d096b-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d096b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d096b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d096b-128">INPUTS</span></span>

### <span data-ttu-id="d096b-129">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="d096b-129">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="d096b-130">Parameters: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d096b-130">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="d096b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d096b-131">OUTPUTS</span></span>

### <span data-ttu-id="d096b-132">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d096b-132">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint</span></span>

## <span data-ttu-id="d096b-133">Note</span><span class="sxs-lookup"><span data-stu-id="d096b-133">NOTES</span></span>

## <span data-ttu-id="d096b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d096b-134">RELATED LINKS</span></span>

[<span data-ttu-id="d096b-135">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="d096b-135">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="d096b-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="d096b-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="d096b-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d096b-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


