---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332800"
---
# <span data-ttu-id="94633-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="94633-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="94633-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94633-102">SYNOPSIS</span></span>
<span data-ttu-id="94633-103">Ottenere o elencare i set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="94633-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="94633-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94633-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94633-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94633-105">DESCRIPTION</span></span>
<span data-ttu-id="94633-106">Ottenere o elencare i set di crittografia del disco.</span><span class="sxs-lookup"><span data-stu-id="94633-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="94633-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94633-107">EXAMPLES</span></span>

### <span data-ttu-id="94633-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94633-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1 -Name enc1;

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="94633-109">Ottenere il set di crittografia del disco ' ENC1'</span><span class="sxs-lookup"><span data-stu-id="94633-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="94633-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="94633-110">Example 2</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="94633-111">Ottenere tutti i set di crittografia disco nel gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="94633-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="94633-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="94633-112">Example 3</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg2
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc3
Name              : enc3
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="94633-113">Ottenere tutti i set di crittografia disco in abbonamento.</span><span class="sxs-lookup"><span data-stu-id="94633-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="94633-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94633-114">PARAMETERS</span></span>

### <span data-ttu-id="94633-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94633-115">-DefaultProfile</span></span>
<span data-ttu-id="94633-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94633-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94633-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="94633-117">-Name</span></span>
<span data-ttu-id="94633-118">Nome del set di crittografia disco.</span><span class="sxs-lookup"><span data-stu-id="94633-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94633-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94633-119">-ResourceGroupName</span></span>
<span data-ttu-id="94633-120">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94633-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94633-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94633-121">CommonParameters</span></span>
<span data-ttu-id="94633-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94633-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94633-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94633-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94633-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94633-124">INPUTS</span></span>

### <span data-ttu-id="94633-125">System. String</span><span class="sxs-lookup"><span data-stu-id="94633-125">System.String</span></span>

## <span data-ttu-id="94633-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94633-126">OUTPUTS</span></span>

### <span data-ttu-id="94633-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="94633-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="94633-128">Note</span><span class="sxs-lookup"><span data-stu-id="94633-128">NOTES</span></span>

## <span data-ttu-id="94633-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94633-129">RELATED LINKS</span></span>
