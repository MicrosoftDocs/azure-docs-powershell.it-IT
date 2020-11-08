---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2A6DDF5F-2906-4DB5-B791-B6BF590261A0
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdf63e9e4d1d8e34dc63cb90c1fa0de15369fbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030027"
---
# <span data-ttu-id="39f71-101">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="39f71-101">Get-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="39f71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39f71-102">SYNOPSIS</span></span>
<span data-ttu-id="39f71-103">Recupera i Vault di ripristino del sito dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="39f71-103">Gets Site Recovery vaults from the current subscription.</span></span>

## <span data-ttu-id="39f71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39f71-104">SYNTAX</span></span>

### <span data-ttu-id="39f71-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39f71-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="39f71-106">ByName</span><span class="sxs-lookup"><span data-stu-id="39f71-106">ByName</span></span>
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="39f71-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39f71-107">DESCRIPTION</span></span>
<span data-ttu-id="39f71-108">Il cmdlet **Get-AzureSiteRecoveryVault** ottiene un elenco dei Vault di ripristino di siti di Azure o di uno specifico Vault di ripristino del sito dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="39f71-108">The **Get-AzureSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="39f71-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39f71-109">EXAMPLES</span></span>

### <span data-ttu-id="39f71-110">Esempio 1: ottenere il Vault attivo</span><span class="sxs-lookup"><span data-stu-id="39f71-110">Example 1: Get the active vault</span></span>
```
PS C:\> Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

<span data-ttu-id="39f71-111">Questo comando consente di ottenere il Vault di ripristino del sito Azure attivo.</span><span class="sxs-lookup"><span data-stu-id="39f71-111">This command gets the active Azure Site Recovery vault.</span></span>

## <span data-ttu-id="39f71-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39f71-112">PARAMETERS</span></span>

### <span data-ttu-id="39f71-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="39f71-113">-Name</span></span>
<span data-ttu-id="39f71-114">Specifica il nome del Vault da ottenere.</span><span class="sxs-lookup"><span data-stu-id="39f71-114">Specifies the name of the vault to get.</span></span>

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

### <span data-ttu-id="39f71-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="39f71-115">-Profile</span></span>
<span data-ttu-id="39f71-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f71-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="39f71-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="39f71-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39f71-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f71-118">CommonParameters</span></span>
<span data-ttu-id="39f71-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f71-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f71-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39f71-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f71-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39f71-121">INPUTS</span></span>

## <span data-ttu-id="39f71-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39f71-122">OUTPUTS</span></span>

## <span data-ttu-id="39f71-123">Note</span><span class="sxs-lookup"><span data-stu-id="39f71-123">NOTES</span></span>

## <span data-ttu-id="39f71-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39f71-124">RELATED LINKS</span></span>

[<span data-ttu-id="39f71-125">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="39f71-125">New-AzureSiteRecoveryVault</span></span>](./New-AzureSiteRecoveryVault.md)


