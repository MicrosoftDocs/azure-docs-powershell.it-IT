---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030028"
---
# <span data-ttu-id="fa483-101">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="fa483-101">Get-AzureSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="fa483-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa483-102">SYNOPSIS</span></span>
<span data-ttu-id="fa483-103">Ottiene le impostazioni per un Vault di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="fa483-103">Gets settings for a Site Recovery vault.</span></span>

## <span data-ttu-id="fa483-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa483-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fa483-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa483-105">DESCRIPTION</span></span>
<span data-ttu-id="fa483-106">Il cmdlet **Get-AzureSiteRecoveryVaultSettings** ottiene le impostazioni relative al Vault di ripristino del sito di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="fa483-106">The **Get-AzureSiteRecoveryVaultSettings** cmdlet gets settings related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="fa483-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa483-107">EXAMPLES</span></span>

### <span data-ttu-id="fa483-108">Esempio 1: ottenere le informazioni sulle impostazioni</span><span class="sxs-lookup"><span data-stu-id="fa483-108">Example 1: Get settings information</span></span>
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="fa483-109">Questo comando ottiene le informazioni sulle impostazioni per l'attuale archivio di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="fa483-109">This command gets settings information for the current  Azure Site Recovery vault.</span></span>

## <span data-ttu-id="fa483-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa483-110">PARAMETERS</span></span>

### <span data-ttu-id="fa483-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="fa483-111">-Profile</span></span>
<span data-ttu-id="fa483-112">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa483-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa483-113">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="fa483-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa483-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa483-114">CommonParameters</span></span>
<span data-ttu-id="fa483-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa483-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa483-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa483-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa483-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa483-117">INPUTS</span></span>

## <span data-ttu-id="fa483-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa483-118">OUTPUTS</span></span>

## <span data-ttu-id="fa483-119">Note</span><span class="sxs-lookup"><span data-stu-id="fa483-119">NOTES</span></span>

## <span data-ttu-id="fa483-120">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa483-120">RELATED LINKS</span></span>

[<span data-ttu-id="fa483-121">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="fa483-121">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="fa483-122">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="fa483-122">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


