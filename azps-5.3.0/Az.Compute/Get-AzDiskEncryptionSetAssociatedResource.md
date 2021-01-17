---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488523"
---
# <span data-ttu-id="25581-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="25581-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="25581-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25581-102">SYNOPSIS</span></span>
<span data-ttu-id="25581-103">Ottiene l'elenco delle risorse associate al set di crittografia del disco specificato.</span><span class="sxs-lookup"><span data-stu-id="25581-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="25581-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25581-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25581-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25581-105">DESCRIPTION</span></span>
<span data-ttu-id="25581-106">Il cmdlet **Get-AzDiskEncryptionSetAssociatedResource** Ottiene l'elenco delle risorse associate al set di crittografia disco specificato.</span><span class="sxs-lookup"><span data-stu-id="25581-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="25581-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25581-107">EXAMPLES</span></span>

### <span data-ttu-id="25581-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="25581-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="25581-109">Il cmdlet recupera le due risorse, "exampleDisk01" e "exampleDisk02", associate al set di crittografia del disco specificato</span><span class="sxs-lookup"><span data-stu-id="25581-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="25581-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25581-110">PARAMETERS</span></span>

### <span data-ttu-id="25581-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25581-111">-DefaultProfile</span></span>
<span data-ttu-id="25581-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25581-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25581-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="25581-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="25581-114">Nome del set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="25581-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25581-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25581-115">-ResourceGroupName</span></span>
<span data-ttu-id="25581-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25581-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25581-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25581-117">CommonParameters</span></span>
<span data-ttu-id="25581-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25581-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25581-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25581-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25581-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25581-120">INPUTS</span></span>

### <span data-ttu-id="25581-121">System. String</span><span class="sxs-lookup"><span data-stu-id="25581-121">System.String</span></span>

## <span data-ttu-id="25581-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25581-122">OUTPUTS</span></span>

### <span data-ttu-id="25581-123">System. Uri []</span><span class="sxs-lookup"><span data-stu-id="25581-123">System.Uri[]</span></span>

## <span data-ttu-id="25581-124">Note</span><span class="sxs-lookup"><span data-stu-id="25581-124">NOTES</span></span>

## <span data-ttu-id="25581-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25581-125">RELATED LINKS</span></span>
