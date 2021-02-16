---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a5701fc6308f1884bbf0237887a223a62a58669
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411586"
---
# <span data-ttu-id="063c8-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="063c8-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="063c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="063c8-102">SYNOPSIS</span></span>
<span data-ttu-id="063c8-103">Recupera informazioni sulle reti gestite da Ripristino siti per il vault corrente.</span><span class="sxs-lookup"><span data-stu-id="063c8-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="063c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="063c8-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="063c8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="063c8-105">DESCRIPTION</span></span>
<span data-ttu-id="063c8-106">Il cmdlet **Get-AzureSiteRecoveryNetwork** ottiene informazioni sulle reti di Ripristino siti di Azure per l'attuale vault di Ripristino siti.</span><span class="sxs-lookup"><span data-stu-id="063c8-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="063c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="063c8-107">EXAMPLES</span></span>

### <span data-ttu-id="063c8-108">Esempio 1: Ottenere reti di ripristino dei siti</span><span class="sxs-lookup"><span data-stu-id="063c8-108">Example 1: Get site recovery networks</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

<span data-ttu-id="063c8-109">Il primo cmdlet del comando recupera i server per l'attuale vault di Azure Site Recovery usando il cmdlet **Get-AzureSiteRecoveryServer.**</span><span class="sxs-lookup"><span data-stu-id="063c8-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="063c8-110">Il comando archivia i server Ripristino siti nella variabile $Servers di matrice.</span><span class="sxs-lookup"><span data-stu-id="063c8-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="063c8-111">Il secondo comando recupera la rete di ripristino del sito per il primo server della $Servers matrice.</span><span class="sxs-lookup"><span data-stu-id="063c8-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="063c8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="063c8-112">PARAMETERS</span></span>

### <span data-ttu-id="063c8-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="063c8-113">-Profile</span></span>
<span data-ttu-id="063c8-114">Specifica il profilo di Azure da cui viene letto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="063c8-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="063c8-115">Se non si specifica un profilo, questo cmdlet legge dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="063c8-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="063c8-116">-Server</span><span class="sxs-lookup"><span data-stu-id="063c8-116">-Server</span></span>
<span data-ttu-id="063c8-117">Specifica un server di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="063c8-117">Specifies a Site Recovery server.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="063c8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063c8-118">CommonParameters</span></span>
<span data-ttu-id="063c8-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="063c8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063c8-120">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="063c8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063c8-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="063c8-121">INPUTS</span></span>

## <span data-ttu-id="063c8-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="063c8-122">OUTPUTS</span></span>

## <span data-ttu-id="063c8-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="063c8-123">NOTES</span></span>

## <span data-ttu-id="063c8-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="063c8-124">RELATED LINKS</span></span>




