---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee948161f101b83a4892441286b760a044e64358
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405823"
---
# <span data-ttu-id="1a997-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1a997-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="1a997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a997-102">SYNOPSIS</span></span>
<span data-ttu-id="1a997-103">Recupera i contenitori di protezione per un vault di Ripristino siti.</span><span class="sxs-lookup"><span data-stu-id="1a997-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="1a997-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a997-104">SYNTAX</span></span>

### <span data-ttu-id="1a997-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a997-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1a997-106">ById</span><span class="sxs-lookup"><span data-stu-id="1a997-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1a997-107">ByName</span><span class="sxs-lookup"><span data-stu-id="1a997-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1a997-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1a997-108">DESCRIPTION</span></span>
<span data-ttu-id="1a997-109">Il cmdlet **Get-AzureSiteRecoveryProtectionContainer** ottiene i contenitori di protezione per l'attuale vault di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1a997-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="1a997-110">Un contenitore di protezione è un contenitore logico per gli oggetti protetti, ad esempio le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="1a997-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="1a997-111">I criteri di protezione definiscono le impostazioni di replica per gli elementi protetti e possono essere associati a un contenitore di protezione e applicati a un'entità protetta.</span><span class="sxs-lookup"><span data-stu-id="1a997-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="1a997-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a997-112">EXAMPLES</span></span>

### <span data-ttu-id="1a997-113">Esempio 1: Ottenere contenitori protetti</span><span class="sxs-lookup"><span data-stu-id="1a997-113">Example 1: Get protected containers</span></span>
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

<span data-ttu-id="1a997-114">Questo comando recupera i contenitori protetti per il vault corrente.</span><span class="sxs-lookup"><span data-stu-id="1a997-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="1a997-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a997-115">PARAMETERS</span></span>

### <span data-ttu-id="1a997-116">-Id</span><span class="sxs-lookup"><span data-stu-id="1a997-116">-Id</span></span>
<span data-ttu-id="1a997-117">Specifica l'ID di un contenitore protetto da ottenere.</span><span class="sxs-lookup"><span data-stu-id="1a997-117">Specifies the ID of a protected container to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a997-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1a997-118">-Name</span></span>
<span data-ttu-id="1a997-119">Specifica il nome di un contenitore di protezione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="1a997-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="1a997-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="1a997-120">-Profile</span></span>
<span data-ttu-id="1a997-121">Specifica il profilo di Azure da cui viene letto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a997-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a997-122">Se non si specifica un profilo, questo cmdlet legge dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1a997-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a997-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a997-123">CommonParameters</span></span>
<span data-ttu-id="1a997-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a997-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a997-125">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a997-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a997-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="1a997-126">INPUTS</span></span>

## <span data-ttu-id="1a997-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a997-127">OUTPUTS</span></span>

## <span data-ttu-id="1a997-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="1a997-128">NOTES</span></span>

## <span data-ttu-id="1a997-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a997-129">RELATED LINKS</span></span>




