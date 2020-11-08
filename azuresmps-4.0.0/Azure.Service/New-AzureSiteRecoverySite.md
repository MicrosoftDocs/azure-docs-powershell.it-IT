---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023850"
---
# <span data-ttu-id="db9dc-101">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="db9dc-101">New-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="db9dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="db9dc-103">Crea un sito di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="db9dc-103">Creates a Site Recovery site.</span></span>

## <span data-ttu-id="db9dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db9dc-104">SYNTAX</span></span>

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="db9dc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db9dc-105">DESCRIPTION</span></span>
<span data-ttu-id="db9dc-106">Il cmdlet **New-AzureSiteRecoverySite** crea un sito di ripristino di Azure sito nel Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="db9dc-106">The **New-AzureSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="db9dc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db9dc-107">EXAMPLES</span></span>

### <span data-ttu-id="db9dc-108">Esempio 1: creare un sito di ripristino del sito</span><span class="sxs-lookup"><span data-stu-id="db9dc-108">Example 1: Create a Site Recovery site</span></span>
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

<span data-ttu-id="db9dc-109">Questo comando crea un sito di ripristino del sito denominato RecoverySite07.</span><span class="sxs-lookup"><span data-stu-id="db9dc-109">This command creates a site recovery site named RecoverySite07.</span></span>

## <span data-ttu-id="db9dc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db9dc-110">PARAMETERS</span></span>

### <span data-ttu-id="db9dc-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="db9dc-111">-Name</span></span>
<span data-ttu-id="db9dc-112">Specifica il nome del sito.</span><span class="sxs-lookup"><span data-stu-id="db9dc-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db9dc-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="db9dc-113">-Profile</span></span>
<span data-ttu-id="db9dc-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db9dc-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db9dc-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="db9dc-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db9dc-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="db9dc-116">-Vault</span></span>
<span data-ttu-id="db9dc-117">Specifica un Vault per cui creare il sito.</span><span class="sxs-lookup"><span data-stu-id="db9dc-117">Specifies a vault for which to create the site.</span></span>
<span data-ttu-id="db9dc-118">Per ottenere un oggetto **ASRVault** , usa il cmdlet **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="db9dc-118">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

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

### <span data-ttu-id="db9dc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9dc-119">CommonParameters</span></span>
<span data-ttu-id="db9dc-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db9dc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9dc-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db9dc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9dc-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db9dc-122">INPUTS</span></span>

## <span data-ttu-id="db9dc-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db9dc-123">OUTPUTS</span></span>

## <span data-ttu-id="db9dc-124">Note</span><span class="sxs-lookup"><span data-stu-id="db9dc-124">NOTES</span></span>

## <span data-ttu-id="db9dc-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db9dc-125">RELATED LINKS</span></span>

[<span data-ttu-id="db9dc-126">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="db9dc-126">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="db9dc-127">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="db9dc-127">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)


