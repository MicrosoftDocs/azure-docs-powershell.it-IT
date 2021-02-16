---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194318"
---
# <span data-ttu-id="93168-101">Modulo Az.ImportExport</span><span class="sxs-lookup"><span data-stu-id="93168-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="93168-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93168-102">Description</span></span>
<span data-ttu-id="93168-103">Microsoft Azure PowerShell: Cmdlet ImportExport</span><span class="sxs-lookup"><span data-stu-id="93168-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="93168-104">Cmdlet Az.ImportExport</span><span class="sxs-lookup"><span data-stu-id="93168-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="93168-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="93168-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="93168-106">Ottiene informazioni su un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="93168-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="93168-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="93168-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="93168-108">Restituisce le chiavi BitLocker per tutte le unità nel processo specificato.</span><span class="sxs-lookup"><span data-stu-id="93168-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="93168-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="93168-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="93168-110">Restituisce i dettagli su una posizione a cui è possibile spedire i dischi associati a un processo di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="93168-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="93168-111">Una posizione è un'area geografica azure.</span><span class="sxs-lookup"><span data-stu-id="93168-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="93168-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="93168-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="93168-113">Crea un nuovo processo o aggiorna un processo esistente nella sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="93168-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="93168-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="93168-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="93168-115">Creare un oggetto DriverList per ImportExport.</span><span class="sxs-lookup"><span data-stu-id="93168-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="93168-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="93168-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="93168-117">Elimina un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="93168-117">Deletes an existing job.</span></span>
<span data-ttu-id="93168-118">È possibile eliminare solo i processi negli stati Creazione o Completata.</span><span class="sxs-lookup"><span data-stu-id="93168-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="93168-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="93168-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="93168-120">Aggiorna proprietà specifiche di un processo.</span><span class="sxs-lookup"><span data-stu-id="93168-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="93168-121">È possibile chiamare questa operazione per notificare al servizio di importazione/esportazione che i dischi rigidi che comprendono il processo di importazione o esportazione sono stati spediti al data center Microsoft.</span><span class="sxs-lookup"><span data-stu-id="93168-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="93168-122">Può anche essere usato per annullare un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="93168-122">It can also be used to cancel an existing job.</span></span>

