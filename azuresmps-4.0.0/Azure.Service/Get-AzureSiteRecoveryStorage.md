---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 78DE0AD2-6210-4604-89A8-41915D58BD68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c40cb0fd38953ff46fa1138dc91f0b9e97ece75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023534"
---
# <span data-ttu-id="cf062-101">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="cf062-101">Get-AzureSiteRecoveryStorage</span></span>

## <span data-ttu-id="cf062-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf062-102">SYNOPSIS</span></span>
<span data-ttu-id="cf062-103">Ottiene gli archivi di ripristino del sito per un Vault.</span><span class="sxs-lookup"><span data-stu-id="cf062-103">Gets Site Recovery Storages for a vault.</span></span>

## <span data-ttu-id="cf062-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf062-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryStorage -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cf062-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf062-105">DESCRIPTION</span></span>
<span data-ttu-id="cf062-106">Il cmdlet **Get-AzureSiteRecoveryStorage** ottiene gli archivi di ripristino del sito di Azure per il Vault di ripristino del sito Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="cf062-106">The **Get-AzureSiteRecoveryStorage** cmdlet gets Azure Site Recovery Storages for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="cf062-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf062-107">EXAMPLES</span></span>

### <span data-ttu-id="cf062-108">Esempio 1: ottenere l'archiviazione di ripristino del sito</span><span class="sxs-lookup"><span data-stu-id="cf062-108">Example 1: Get site recovery storage</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryStorage -Server $Servers[0]
Name           : phase2PrimaryStorageClassification
ID             : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
FabricObjectID : 1c1d0c0b-0c50-4675-af1a-1fdac70dbb6d
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM

Name           : phase2RecoveryStorageClassification
ID             : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
FabricObjectID : 20cf8d92-fd5d-4872-985a-0f4562b8a0bf
ServerId       : 774859b0-1966-48cc-9df7-759c441b7a8c
Type           : Classification
FabricType     : VMM
```

<span data-ttu-id="cf062-109">Il primo cmdlet di comando ottiene i server per il Vault di ripristino del sito Azure corrente usando il cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="cf062-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="cf062-110">Il comando Archivia i server di ripristino del sito nella variabile di matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="cf062-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="cf062-111">Il secondo comando consente di ottenere l'archiviazione di ripristino del sito per il primo server nella matrice $Servers.</span><span class="sxs-lookup"><span data-stu-id="cf062-111">The second command gets the site recovery storage for the first server in the $Servers array.</span></span>

## <span data-ttu-id="cf062-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf062-112">PARAMETERS</span></span>

### <span data-ttu-id="cf062-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="cf062-113">-Profile</span></span>
<span data-ttu-id="cf062-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf062-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cf062-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="cf062-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cf062-116">-Server</span><span class="sxs-lookup"><span data-stu-id="cf062-116">-Server</span></span>
<span data-ttu-id="cf062-117">Specifica un server per l'archiviazione di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="cf062-117">Specifies a server for Azure Site Recovery Storage.</span></span>
<span data-ttu-id="cf062-118">Per ottenere un oggetto **ASRServer** , usa il cmdlet **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="cf062-118">To obtain an **ASRServer** object, use the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>

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

### <span data-ttu-id="cf062-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf062-119">CommonParameters</span></span>
<span data-ttu-id="cf062-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf062-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf062-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf062-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf062-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf062-122">INPUTS</span></span>

## <span data-ttu-id="cf062-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf062-123">OUTPUTS</span></span>

## <span data-ttu-id="cf062-124">Note</span><span class="sxs-lookup"><span data-stu-id="cf062-124">NOTES</span></span>

## <span data-ttu-id="cf062-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf062-125">RELATED LINKS</span></span>

[<span data-ttu-id="cf062-126">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="cf062-126">Get-AzureSiteRecoveryServer</span></span>](./Get-AzureSiteRecoveryServer.md)


