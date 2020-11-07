---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 22e49dc0ebb5c38a1b260f72cc4fe97294bf5505
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677704"
---
# <span data-ttu-id="2a2a5-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="2a2a5-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="2a2a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2a5-103">Ottenere i dettagli di un tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2a5-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="2a2a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a2a5-104">SYNTAX</span></span>

### <span data-ttu-id="2a2a5-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a2a5-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a2a5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2a2a5-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a2a5-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2a2a5-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a2a5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a2a5-108">DESCRIPTION</span></span>
<span data-ttu-id="2a2a5-109">Il cmdlet **Get-AzRecoveryServicesAsrFabric** ottiene le proprietà di un determinato tessuto di recupero del sito di Azure o di tutti i tessuti di ripristino di Azure site in un caveau di un servizio di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2a2a5-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="2a2a5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a2a5-110">EXAMPLES</span></span>

### <span data-ttu-id="2a2a5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2a2a5-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="2a2a5-112">Restituisce tutti i tessuti di ripristino di Azure site nel Vault.</span><span class="sxs-lookup"><span data-stu-id="2a2a5-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="2a2a5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2a2a5-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="2a2a5-114">Restituisce il tessuto di recupero sito di Azure con nome xxxx.</span><span class="sxs-lookup"><span data-stu-id="2a2a5-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="2a2a5-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="2a2a5-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="2a2a5-116">Restituisce il tessuto di recupero sito di Azure con nome descrittivo xxxx.</span><span class="sxs-lookup"><span data-stu-id="2a2a5-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="2a2a5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a2a5-117">PARAMETERS</span></span>

### <span data-ttu-id="2a2a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2a5-118">-DefaultProfile</span></span>
<span data-ttu-id="2a2a5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a2a5-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2a2a5-120">-FriendlyName</span></span>
<span data-ttu-id="2a2a5-121">Cercare il tessuto ASR con il nome descrittivo del tessuto.</span><span class="sxs-lookup"><span data-stu-id="2a2a5-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="2a2a5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a2a5-122">-Name</span></span>
<span data-ttu-id="2a2a5-123">Cercare il tessuto ASR in base al nome del tessuto.</span><span class="sxs-lookup"><span data-stu-id="2a2a5-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="2a2a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2a5-124">CommonParameters</span></span>
<span data-ttu-id="2a2a5-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a2a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2a5-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a2a5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2a5-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a2a5-127">INPUTS</span></span>

### <span data-ttu-id="2a2a5-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2a2a5-128">None</span></span>

## <span data-ttu-id="2a2a5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a2a5-129">OUTPUTS</span></span>

### <span data-ttu-id="2a2a5-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2a2a5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2a2a5-131">Note</span><span class="sxs-lookup"><span data-stu-id="2a2a5-131">NOTES</span></span>

## <span data-ttu-id="2a2a5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a2a5-132">RELATED LINKS</span></span>

[<span data-ttu-id="2a2a5-133">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="2a2a5-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="2a2a5-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="2a2a5-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
