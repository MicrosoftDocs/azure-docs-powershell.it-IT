---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 0a5c5f42f7a6f4755335a5b8827fd2d23e096679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511327"
---
# <span data-ttu-id="69c61-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="69c61-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="69c61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69c61-102">SYNOPSIS</span></span>
<span data-ttu-id="69c61-103">Ottiene i punti di ripristino per un elemento di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="69c61-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69c61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69c61-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69c61-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69c61-105">DESCRIPTION</span></span>
<span data-ttu-id="69c61-106">Il cmdlet **Get-AzureRmBackupRecoveryPoint** ottiene i punti di ripristino per un elemento di backup di Azure supportato.</span><span class="sxs-lookup"><span data-stu-id="69c61-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="69c61-107">Dopo aver eseguito il backup di un elemento, il backup archivia uno o più punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="69c61-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="69c61-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69c61-108">EXAMPLES</span></span>

### <span data-ttu-id="69c61-109">Esempio 1: ottenere punti di ripristino per un elemento</span><span class="sxs-lookup"><span data-stu-id="69c61-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="69c61-110">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="69c61-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="69c61-111">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="69c61-111">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="69c61-112">Il secondo comando ottiene un contenitore con il nome specificato nel Vault in $Vault usando il cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="69c61-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="69c61-113">Il comando Archivia l'oggetto nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="69c61-113">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="69c61-114">Il terzo comando ottiene l'elemento di backup nel contenitore in $Container usando il cmdlet **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="69c61-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="69c61-115">Il comando Archivia l'oggetto nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="69c61-115">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="69c61-116">Il comando finale ottiene i punti di ripristino per l'elemento in $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="69c61-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="69c61-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69c61-117">PARAMETERS</span></span>

### <span data-ttu-id="69c61-118">-Elemento</span><span class="sxs-lookup"><span data-stu-id="69c61-118">-Item</span></span>
<span data-ttu-id="69c61-119">Specifica l'elemento per cui questo cmdlet ottiene i punti di ripristino.</span><span class="sxs-lookup"><span data-stu-id="69c61-119">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="69c61-120">Per ottenere un **AzureRmBackupItem** , usare il cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="69c61-120">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="69c61-121">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="69c61-121">-RecoveryPointId</span></span>
<span data-ttu-id="69c61-122">Specifica l'ID di un punto di recupero ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69c61-122">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

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

### <span data-ttu-id="69c61-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c61-123">-DefaultProfile</span></span>
<span data-ttu-id="69c61-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69c61-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69c61-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c61-125">CommonParameters</span></span>
<span data-ttu-id="69c61-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c61-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c61-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69c61-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c61-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69c61-128">INPUTS</span></span>

### <span data-ttu-id="69c61-129">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="69c61-129">AzureRmBackupItem</span></span>

## <span data-ttu-id="69c61-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69c61-130">OUTPUTS</span></span>

### <span data-ttu-id="69c61-131">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="69c61-131">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="69c61-132">Note</span><span class="sxs-lookup"><span data-stu-id="69c61-132">NOTES</span></span>

## <span data-ttu-id="69c61-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69c61-133">RELATED LINKS</span></span>

[<span data-ttu-id="69c61-134">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="69c61-134">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="69c61-135">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="69c61-135">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="69c61-136">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="69c61-136">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


