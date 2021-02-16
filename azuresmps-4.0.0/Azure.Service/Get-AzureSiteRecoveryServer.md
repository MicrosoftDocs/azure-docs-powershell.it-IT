---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79b61501a56913fedb2a003d7aea1a041bfab4d5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412283"
---
# <span data-ttu-id="50894-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="50894-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="50894-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50894-102">SYNOPSIS</span></span>
<span data-ttu-id="50894-103">Recupera i server di ripristino del sito registrati in un vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="50894-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="50894-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50894-104">SYNTAX</span></span>

### <span data-ttu-id="50894-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50894-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="50894-106">ById</span><span class="sxs-lookup"><span data-stu-id="50894-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="50894-107">ByName</span><span class="sxs-lookup"><span data-stu-id="50894-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="50894-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="50894-108">DESCRIPTION</span></span>
<span data-ttu-id="50894-109">Il cmdlet **Get-AzureSiteRecoveryServer** ottiene informazioni sui server di Azure Site Recovery registrati nel vault di Ripristino siti corrente.</span><span class="sxs-lookup"><span data-stu-id="50894-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="50894-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50894-110">EXAMPLES</span></span>

### <span data-ttu-id="50894-111">Esempio 1: Ottenere informazioni su un server Ripristino siti</span><span class="sxs-lookup"><span data-stu-id="50894-111">Example 1: Get information about a Site Recovery server</span></span>
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

<span data-ttu-id="50894-112">Questo comando ottiene informazioni su un server Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="50894-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="50894-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50894-113">PARAMETERS</span></span>

### <span data-ttu-id="50894-114">-Id</span><span class="sxs-lookup"><span data-stu-id="50894-114">-Id</span></span>
<span data-ttu-id="50894-115">Specifica l'ID di un server.</span><span class="sxs-lookup"><span data-stu-id="50894-115">Specifies the ID of a server.</span></span>

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

### <span data-ttu-id="50894-116">-Name</span><span class="sxs-lookup"><span data-stu-id="50894-116">-Name</span></span>
<span data-ttu-id="50894-117">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="50894-117">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="50894-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="50894-118">-Profile</span></span>
<span data-ttu-id="50894-119">Specifica il profilo di Azure da cui viene letto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50894-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="50894-120">Se non si specifica un profilo, questo cmdlet legge dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="50894-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50894-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50894-121">CommonParameters</span></span>
<span data-ttu-id="50894-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50894-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50894-123">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50894-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50894-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="50894-124">INPUTS</span></span>

## <span data-ttu-id="50894-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50894-125">OUTPUTS</span></span>

## <span data-ttu-id="50894-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="50894-126">NOTES</span></span>

## <span data-ttu-id="50894-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50894-127">RELATED LINKS</span></span>




