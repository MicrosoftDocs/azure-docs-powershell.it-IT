---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 92631a1a6c5d27953777efe2b6ea158f59da8fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509696"
---
# <span data-ttu-id="de17f-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="de17f-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="de17f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de17f-102">SYNOPSIS</span></span>
<span data-ttu-id="de17f-103">Ottenere i dettagli di un tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="de17f-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de17f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de17f-104">SYNTAX</span></span>

### <span data-ttu-id="de17f-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de17f-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de17f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="de17f-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de17f-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="de17f-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de17f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de17f-108">DESCRIPTION</span></span>
<span data-ttu-id="de17f-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrFabric** ottiene le proprietà di un determinato tessuto di recupero del sito di Azure o di tutti i tessuti di ripristino di Azure site in un caveau di un servizio di ripristino.</span><span class="sxs-lookup"><span data-stu-id="de17f-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="de17f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de17f-110">EXAMPLES</span></span>

### <span data-ttu-id="de17f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de17f-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="de17f-112">Restituisce tutti i tessuti di ripristino di Azure site nel Vault.</span><span class="sxs-lookup"><span data-stu-id="de17f-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="de17f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="de17f-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="de17f-114">Restituisce il tessuto di recupero sito di Azure con nome xxxx.</span><span class="sxs-lookup"><span data-stu-id="de17f-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="de17f-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="de17f-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="de17f-116">Restituisce il tessuto di recupero sito di Azure con nome descrittivo xxxx.</span><span class="sxs-lookup"><span data-stu-id="de17f-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="de17f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de17f-117">PARAMETERS</span></span>

### <span data-ttu-id="de17f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de17f-118">-DefaultProfile</span></span>
<span data-ttu-id="de17f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de17f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="de17f-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="de17f-120">-FriendlyName</span></span>
<span data-ttu-id="de17f-121">Cercare il tessuto ASR con il nome descrittivo del tessuto.</span><span class="sxs-lookup"><span data-stu-id="de17f-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de17f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="de17f-122">-Name</span></span>
<span data-ttu-id="de17f-123">Cercare il tessuto ASR in base al nome del tessuto.</span><span class="sxs-lookup"><span data-stu-id="de17f-123">Search for the ASR fabric by the name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de17f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de17f-124">CommonParameters</span></span>
<span data-ttu-id="de17f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de17f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de17f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de17f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de17f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de17f-127">INPUTS</span></span>

### <span data-ttu-id="de17f-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="de17f-128">None</span></span>

## <span data-ttu-id="de17f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de17f-129">OUTPUTS</span></span>

### <span data-ttu-id="de17f-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="de17f-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="de17f-131">Note</span><span class="sxs-lookup"><span data-stu-id="de17f-131">NOTES</span></span>

## <span data-ttu-id="de17f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de17f-132">RELATED LINKS</span></span>

[<span data-ttu-id="de17f-133">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="de17f-133">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="de17f-134">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="de17f-134">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)