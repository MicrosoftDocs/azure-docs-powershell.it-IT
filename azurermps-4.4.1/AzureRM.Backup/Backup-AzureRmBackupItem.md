---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1cb5ccf56a2ef6888231ca81df0e352f5d505e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510776"
---
# <span data-ttu-id="b7c9c-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="b7c9c-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="b7c9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c9c-103">Avvia un backup per un elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7c9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7c9c-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7c9c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7c9c-105">DESCRIPTION</span></span>
<span data-ttu-id="b7c9c-106">Il cmdlet **backup-AzureRmBackupItem** avvia un backup per un elemento di backup di Azure protetto che non è legato alla pianificazione del backup.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="b7c9c-107">È possibile eseguire un backup iniziale subito dopo l'abilitazione della protezione o avviare un backup dopo un errore di backup pianificato.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="b7c9c-108">Se è in corso un processo di backup esistente, il cmdlet non riesce.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="b7c9c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7c9c-109">EXAMPLES</span></span>

### <span data-ttu-id="b7c9c-110">Esempio 1: iniziare a eseguire il backup di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b7c9c-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="b7c9c-111">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="b7c9c-112">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="b7c9c-113">Il secondo comando ottiene un contenitore con il nome specificato nel Vault in $Vault usando il cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="b7c9c-114">Il comando Archivia l'oggetto nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="b7c9c-115">L'ultimo comando ottiene gli elementi di backup in $Container usando il cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="b7c9c-116">Il comando passa gli elementi al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b7c9c-117">Il cmdlet corrente avvia il backup della macchina virtuale nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="b7c9c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7c9c-118">PARAMETERS</span></span>

### <span data-ttu-id="b7c9c-119">-Elemento</span><span class="sxs-lookup"><span data-stu-id="b7c9c-119">-Item</span></span>
<span data-ttu-id="b7c9c-120">Specifica un elemento di backup per il quale questo cmdlet avvia un'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="b7c9c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c9c-121">-DefaultProfile</span></span>
<span data-ttu-id="b7c9c-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7c9c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c9c-123">CommonParameters</span></span>
<span data-ttu-id="b7c9c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c9c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c9c-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c9c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c9c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7c9c-126">INPUTS</span></span>

### <span data-ttu-id="b7c9c-127">AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="b7c9c-127">AzureRMBackupItem</span></span>

## <span data-ttu-id="b7c9c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7c9c-128">OUTPUTS</span></span>

### <span data-ttu-id="b7c9c-129">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="b7c9c-129">AzureRmBackupJob</span></span>

## <span data-ttu-id="b7c9c-130">Note</span><span class="sxs-lookup"><span data-stu-id="b7c9c-130">NOTES</span></span>

## <span data-ttu-id="b7c9c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7c9c-131">RELATED LINKS</span></span>

[<span data-ttu-id="b7c9c-132">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="b7c9c-132">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="b7c9c-133">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b7c9c-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="b7c9c-134">Ripristinare-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="b7c9c-134">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


