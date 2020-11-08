---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023932"
---
# <span data-ttu-id="bb45d-101">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="bb45d-101">New-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="bb45d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb45d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb45d-103">Crea un Vault di servizi di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="bb45d-103">Creates a Site Recovery services vault.</span></span>

## <span data-ttu-id="bb45d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb45d-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bb45d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb45d-105">DESCRIPTION</span></span>
<span data-ttu-id="bb45d-106">Il cmdlet **New-AzureSiteRecoveryVault** crea un Vault di servizi di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="bb45d-106">The **New-AzureSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="bb45d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb45d-107">EXAMPLES</span></span>

### <span data-ttu-id="bb45d-108">Esempio 1: creare un Vault</span><span class="sxs-lookup"><span data-stu-id="bb45d-108">Example 1: Create a vault</span></span>
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

<span data-ttu-id="bb45d-109">Questo comando crea un Vault denominato ContosoVault nella posizione ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="bb45d-109">This command creates a vault named ContosoVault in the West US location.</span></span>

## <span data-ttu-id="bb45d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb45d-110">PARAMETERS</span></span>

### <span data-ttu-id="bb45d-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="bb45d-111">-Location</span></span>
<span data-ttu-id="bb45d-112">Specifica la posizione geografica.</span><span class="sxs-lookup"><span data-stu-id="bb45d-112">Specifies the geographical location.</span></span>

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

### <span data-ttu-id="bb45d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb45d-113">-Name</span></span>
<span data-ttu-id="bb45d-114">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="bb45d-114">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="bb45d-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="bb45d-115">-Profile</span></span>
<span data-ttu-id="bb45d-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb45d-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bb45d-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="bb45d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bb45d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb45d-118">CommonParameters</span></span>
<span data-ttu-id="bb45d-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb45d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb45d-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb45d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb45d-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb45d-121">INPUTS</span></span>

## <span data-ttu-id="bb45d-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb45d-122">OUTPUTS</span></span>

## <span data-ttu-id="bb45d-123">Note</span><span class="sxs-lookup"><span data-stu-id="bb45d-123">NOTES</span></span>

## <span data-ttu-id="bb45d-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb45d-124">RELATED LINKS</span></span>

[<span data-ttu-id="bb45d-125">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="bb45d-125">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)


