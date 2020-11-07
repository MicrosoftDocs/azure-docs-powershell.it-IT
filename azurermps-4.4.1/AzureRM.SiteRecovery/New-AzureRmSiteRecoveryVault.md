---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 786e3c17ca64acf908d06b88462f44af502e36c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686146"
---
# <span data-ttu-id="43d1c-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="43d1c-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="43d1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="43d1c-103">Crea un Vault di servizi di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="43d1c-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43d1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43d1c-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43d1c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43d1c-105">DESCRIPTION</span></span>
<span data-ttu-id="43d1c-106">Il cmdlet **New-AzureRmSiteRecoveryVault** crea un Vault di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="43d1c-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="43d1c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43d1c-107">EXAMPLES</span></span>

## <span data-ttu-id="43d1c-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43d1c-108">PARAMETERS</span></span>

### <span data-ttu-id="43d1c-109">-Posizione</span><span class="sxs-lookup"><span data-stu-id="43d1c-109">-Location</span></span>
<span data-ttu-id="43d1c-110">Specifica il nome della posizione geografica.</span><span class="sxs-lookup"><span data-stu-id="43d1c-110">Specifies the geographical location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d1c-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="43d1c-111">-Name</span></span>
<span data-ttu-id="43d1c-112">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="43d1c-112">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d1c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d1c-113">-ResourceGroupName</span></span>
<span data-ttu-id="43d1c-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43d1c-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d1c-115">-DefaultProfile</span></span>
<span data-ttu-id="43d1c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43d1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d1c-117">CommonParameters</span></span>
<span data-ttu-id="43d1c-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d1c-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43d1c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d1c-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43d1c-120">INPUTS</span></span>

## <span data-ttu-id="43d1c-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43d1c-121">OUTPUTS</span></span>

## <span data-ttu-id="43d1c-122">Note</span><span class="sxs-lookup"><span data-stu-id="43d1c-122">NOTES</span></span>

## <span data-ttu-id="43d1c-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43d1c-123">RELATED LINKS</span></span>

[<span data-ttu-id="43d1c-124">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="43d1c-124">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="43d1c-125">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="43d1c-125">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
