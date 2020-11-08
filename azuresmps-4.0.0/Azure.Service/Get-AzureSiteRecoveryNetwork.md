---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96b51b49d76093be96eeab26417f4a70f70c4627
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023550"
---
# <span data-ttu-id="68586-101">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="68586-101">Get-AzureSiteRecoveryNetwork</span></span>

## <span data-ttu-id="68586-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68586-102">SYNOPSIS</span></span>
<span data-ttu-id="68586-103">Ottiene informazioni sulle reti gestite dal ripristino del sito per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="68586-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="68586-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68586-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="68586-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68586-105">DESCRIPTION</span></span>
<span data-ttu-id="68586-106">Il cmdlet **Get-AzureSiteRecoveryNetwork** ottiene informazioni sulle reti di ripristino dei siti di Azure per il Vault di ripristino del sito corrente.</span><span class="sxs-lookup"><span data-stu-id="68586-106">The **Get-AzureSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Site Recovery vault.</span></span>

## <span data-ttu-id="68586-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68586-107">EXAMPLES</span></span>

### <span data-ttu-id="68586-108">Esempio 1: ottenere reti di ripristino del sito</span><span class="sxs-lookup"><span data-stu-id="68586-108">Example 1: Get site recovery networks</span></span>
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

<span data-ttu-id="68586-109">Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito Azure corrente usando il cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="68586-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="68586-110">Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="68586-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="68586-111">Il secondo comando consente di ottenere la rete di ripristino del sito per il primo server nella matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="68586-111">The second command gets the site recovery network for the first server in the $Servers array.</span></span>

## <span data-ttu-id="68586-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68586-112">PARAMETERS</span></span>

### <span data-ttu-id="68586-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="68586-113">-Profile</span></span>
<span data-ttu-id="68586-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68586-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="68586-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="68586-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="68586-116">-Server</span><span class="sxs-lookup"><span data-stu-id="68586-116">-Server</span></span>
<span data-ttu-id="68586-117">Specifica un server di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="68586-117">Specifies a Site Recovery server.</span></span>

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

### <span data-ttu-id="68586-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68586-118">CommonParameters</span></span>
<span data-ttu-id="68586-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68586-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68586-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68586-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68586-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68586-121">INPUTS</span></span>

## <span data-ttu-id="68586-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68586-122">OUTPUTS</span></span>

## <span data-ttu-id="68586-123">Note</span><span class="sxs-lookup"><span data-stu-id="68586-123">NOTES</span></span>

## <span data-ttu-id="68586-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68586-124">RELATED LINKS</span></span>

[<span data-ttu-id="68586-125">Cmdlet di servizi di ripristino siti di Azure</span><span class="sxs-lookup"><span data-stu-id="68586-125">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


