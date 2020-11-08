---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023535"
---
# <span data-ttu-id="eb91a-101">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="eb91a-101">Get-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="eb91a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb91a-102">SYNOPSIS</span></span>
<span data-ttu-id="eb91a-103">Ottiene i siti Hyper-V da un Vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="eb91a-103">Gets the Hyper-V sites from a Site Recovery vault.</span></span>

## <span data-ttu-id="eb91a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb91a-104">SYNTAX</span></span>

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="eb91a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb91a-105">DESCRIPTION</span></span>
<span data-ttu-id="eb91a-106">Il cmdlet **Get-AzureSiteRecoverySite** ottiene i siti Hyper-V in un Vault di ripristino di un sito Azure.</span><span class="sxs-lookup"><span data-stu-id="eb91a-106">The **Get-AzureSiteRecoverySite** cmdlet gets the Hyper-V sites in an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="eb91a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb91a-107">EXAMPLES</span></span>

### <span data-ttu-id="eb91a-108">Esempio 1: ottenere siti di ripristino</span><span class="sxs-lookup"><span data-stu-id="eb91a-108">Example 1: Get recovery sites</span></span>
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

<span data-ttu-id="eb91a-109">Questo comando consente di ottenere i siti di recupero per il Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="eb91a-109">This command gets the recovery sites for the current vault.</span></span>

## <span data-ttu-id="eb91a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb91a-110">PARAMETERS</span></span>

### <span data-ttu-id="eb91a-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="eb91a-111">-Profile</span></span>
<span data-ttu-id="eb91a-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb91a-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb91a-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="eb91a-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb91a-114">-Vault</span><span class="sxs-lookup"><span data-stu-id="eb91a-114">-Vault</span></span>
<span data-ttu-id="eb91a-115">Specifica un Vault per cui ottenere i siti.</span><span class="sxs-lookup"><span data-stu-id="eb91a-115">Specifies a vault for which to get sites.</span></span>
<span data-ttu-id="eb91a-116">Per ottenere un oggetto **ASRVault** , usa il cmdlet **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="eb91a-116">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb91a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb91a-117">CommonParameters</span></span>
<span data-ttu-id="eb91a-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb91a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb91a-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb91a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb91a-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb91a-120">INPUTS</span></span>

## <span data-ttu-id="eb91a-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb91a-121">OUTPUTS</span></span>

## <span data-ttu-id="eb91a-122">Note</span><span class="sxs-lookup"><span data-stu-id="eb91a-122">NOTES</span></span>

## <span data-ttu-id="eb91a-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb91a-123">RELATED LINKS</span></span>

[<span data-ttu-id="eb91a-124">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="eb91a-124">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="eb91a-125">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="eb91a-125">New-AzureSiteRecoverySite</span></span>](./New-AzureSiteRecoverySite.md)


