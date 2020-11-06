---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 74c358935efff57f2caf9fb7b6bd8b75e429aeab
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490409"
---
# <span data-ttu-id="28259-101">Modulo AZS. Compute. admin</span><span class="sxs-lookup"><span data-stu-id="28259-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="28259-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28259-102">Description</span></span>
<span data-ttu-id="28259-103">Versione di anteprima del modulo operatore di calcolo AzureStack che fornisce funzionalità per gestire le quote di calcolo, le immagini della piattaforma e le estensioni della macchina virtuale, nonché i processi di migrazione dei dischi gestiti per riequilibrare lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="28259-103">Preview release of the AzureStack Compute operator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="28259-104">Cmdlet AZS. Compute. admin</span><span class="sxs-lookup"><span data-stu-id="28259-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="28259-105">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="28259-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="28259-106">Aggiungere un'immagine della piattaforma macchina virtuale da una configurazione di immagine specificata.</span><span class="sxs-lookup"><span data-stu-id="28259-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="28259-107">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="28259-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="28259-108">Creare una nuova immagine dell'estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="28259-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="28259-109">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="28259-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="28259-110">Restituisce le quote che specificano i limiti di quota per gli oggetti COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="28259-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="28259-111">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="28259-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="28259-112">Restituisce l'elenco dei dischi gestiti di cui è possibile eseguire la migrazione nella condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="28259-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="28259-113">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="28259-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="28259-114">Restituisce l'elenco dei processi di migrazione del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="28259-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="28259-115">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="28259-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="28259-116">Restituisce le immagini della macchina virtuale caricate nel repository di immagini della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="28259-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="28259-117">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="28259-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="28259-118">Restituisce le estensioni delle immagini della macchina virtuale attualmente disponibili.</span><span class="sxs-lookup"><span data-stu-id="28259-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="28259-119">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="28259-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="28259-120">Creare una nuova quota di calcolo usata per limitare le risorse di calcolo.</span><span class="sxs-lookup"><span data-stu-id="28259-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="28259-121">New-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="28259-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="28259-122">Avvia un processo di migrazione del disco gestito per eseguire la migrazione dei dischi gestiti alla condivisione di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="28259-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="28259-123">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="28259-123">New-DataDiskObject</span></span>](New-DataDiskObject.md)
<span data-ttu-id="28259-124">Crea un disco di dati usato per creare una nuova immagine della piattaforma della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="28259-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="28259-125">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="28259-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="28259-126">Elimina la quota di calcolo specificata.</span><span class="sxs-lookup"><span data-stu-id="28259-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="28259-127">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="28259-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="28259-128">Eliminare un'immagine della macchina virtuale dal repository di immagini della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="28259-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="28259-129">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="28259-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="28259-130">Elimina un'immagine dell'estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="28259-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="28259-131">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="28259-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="28259-132">Aggiornare una quota di calcolo esistente usando i parametri forniti.</span><span class="sxs-lookup"><span data-stu-id="28259-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="28259-133">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="28259-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="28259-134">Annullare un processo di migrazione su disco gestito.</span><span class="sxs-lookup"><span data-stu-id="28259-134">Cancel a managed disk migration job.</span></span>

