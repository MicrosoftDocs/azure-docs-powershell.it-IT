---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4081d6d072aadd6a4ae7d09ff57748a8f2cb697
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023538"
---
# <span data-ttu-id="1e8c5-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="1e8c5-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="1e8c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e8c5-102">SYNOPSIS</span></span>
<span data-ttu-id="1e8c5-103">Recupera i server di ripristino del sito registrato un Vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="1e8c5-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="1e8c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e8c5-104">SYNTAX</span></span>

### <span data-ttu-id="1e8c5-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e8c5-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1e8c5-106">ById</span><span class="sxs-lookup"><span data-stu-id="1e8c5-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1e8c5-107">ByName</span><span class="sxs-lookup"><span data-stu-id="1e8c5-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1e8c5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e8c5-108">DESCRIPTION</span></span>
<span data-ttu-id="1e8c5-109">Il cmdlet **Get-AzureSiteRecoveryServer** ottiene informazioni sui server di ripristino dei siti di Azure registrati nell'attuale archivio di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="1e8c5-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="1e8c5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e8c5-110">EXAMPLES</span></span>

### <span data-ttu-id="1e8c5-111">Esempio 1: ottenere informazioni su un server di ripristino del sito</span><span class="sxs-lookup"><span data-stu-id="1e8c5-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="1e8c5-112">Questo comando consente di ottenere informazioni su un server di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="1e8c5-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="1e8c5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e8c5-113">PARAMETERS</span></span>

### <span data-ttu-id="1e8c5-114">-ID</span><span class="sxs-lookup"><span data-stu-id="1e8c5-114">-Id</span></span>
<span data-ttu-id="1e8c5-115">Specifica l'ID di un server.</span><span class="sxs-lookup"><span data-stu-id="1e8c5-115">Specifies the ID of a server.</span></span>

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

### <span data-ttu-id="1e8c5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e8c5-116">-Name</span></span>
<span data-ttu-id="1e8c5-117">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="1e8c5-117">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="1e8c5-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="1e8c5-118">-Profile</span></span>
<span data-ttu-id="1e8c5-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e8c5-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e8c5-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1e8c5-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e8c5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e8c5-121">CommonParameters</span></span>
<span data-ttu-id="1e8c5-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e8c5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e8c5-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e8c5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e8c5-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e8c5-124">INPUTS</span></span>

## <span data-ttu-id="1e8c5-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e8c5-125">OUTPUTS</span></span>

## <span data-ttu-id="1e8c5-126">Note</span><span class="sxs-lookup"><span data-stu-id="1e8c5-126">NOTES</span></span>

## <span data-ttu-id="1e8c5-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e8c5-127">RELATED LINKS</span></span>

[<span data-ttu-id="1e8c5-128">Cmdlet di servizi di ripristino siti di Azure</span><span class="sxs-lookup"><span data-stu-id="1e8c5-128">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


