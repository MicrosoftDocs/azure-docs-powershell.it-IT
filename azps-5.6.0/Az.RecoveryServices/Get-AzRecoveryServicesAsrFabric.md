---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 1aeaba2f4f25abd49f12d087b7390f5e92f19c3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016157"
---
# <span data-ttu-id="6ddac-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6ddac-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="6ddac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ddac-102">SYNOPSIS</span></span>
<span data-ttu-id="6ddac-103">Ottenere i dettagli di un tessuto azure site recovery.</span><span class="sxs-lookup"><span data-stu-id="6ddac-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="6ddac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ddac-104">SYNTAX</span></span>

### <span data-ttu-id="6ddac-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ddac-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ddac-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6ddac-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ddac-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6ddac-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ddac-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6ddac-108">DESCRIPTION</span></span>
<span data-ttu-id="6ddac-109">Il cmdlet **Get-AzRecoveryServicesAsrFabric** ottiene le proprietà di uno specificato Azure Site Recovery Fabric o di tutti i tessuto di Azure Site Recovery in un vault del servizio di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6ddac-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="6ddac-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ddac-110">EXAMPLES</span></span>

### <span data-ttu-id="6ddac-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ddac-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="6ddac-112">Restituisce tutti i tessuto di Azure Site Recovery nel Vault.</span><span class="sxs-lookup"><span data-stu-id="6ddac-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="6ddac-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6ddac-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="6ddac-114">Restituire tessuto azure site recovery con nome xxxx.</span><span class="sxs-lookup"><span data-stu-id="6ddac-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="6ddac-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6ddac-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="6ddac-116">Restituire tessuto azure site recovery con nome descrittivo xxxx.</span><span class="sxs-lookup"><span data-stu-id="6ddac-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="6ddac-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ddac-117">PARAMETERS</span></span>

### <span data-ttu-id="6ddac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ddac-118">-DefaultProfile</span></span>
<span data-ttu-id="6ddac-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ddac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ddac-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6ddac-120">-FriendlyName</span></span>
<span data-ttu-id="6ddac-121">Cercare il tessuto ASR usando il nome descrittivo del tessuto.</span><span class="sxs-lookup"><span data-stu-id="6ddac-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6ddac-122">-Name</span></span>
<span data-ttu-id="6ddac-123">Cercare il tessuto ASR con il nome del tessuto.</span><span class="sxs-lookup"><span data-stu-id="6ddac-123">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ddac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ddac-124">CommonParameters</span></span>
<span data-ttu-id="6ddac-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ddac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ddac-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6ddac-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ddac-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="6ddac-127">INPUTS</span></span>

### <span data-ttu-id="6ddac-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6ddac-128">None</span></span>

## <span data-ttu-id="6ddac-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ddac-129">OUTPUTS</span></span>

### <span data-ttu-id="6ddac-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6ddac-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6ddac-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="6ddac-131">NOTES</span></span>

## <span data-ttu-id="6ddac-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ddac-132">RELATED LINKS</span></span>

[<span data-ttu-id="6ddac-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6ddac-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="6ddac-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6ddac-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
