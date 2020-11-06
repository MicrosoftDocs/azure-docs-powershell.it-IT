---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 52535af7a2e7e9282a94c07f62154e42fe807a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520623"
---
# <span data-ttu-id="8801a-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="8801a-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="8801a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8801a-102">SYNOPSIS</span></span>
<span data-ttu-id="8801a-103">Ottiene le informazioni sulle impostazioni del Vault ASR per il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8801a-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8801a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8801a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8801a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8801a-105">DESCRIPTION</span></span>
<span data-ttu-id="8801a-106">Il cmdlet **Get-AzureRmRecoveryServicesAsrVaultContext** ottiene le informazioni sulle impostazioni del Vault ASR correlate al Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8801a-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="8801a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8801a-107">EXAMPLES</span></span>

### <span data-ttu-id="8801a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8801a-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="8801a-109">Ottiene le impostazioni del Vault ASR per il Vault dei servizi di ripristino attualmente attivo (nella sessione di PowerShell).</span><span class="sxs-lookup"><span data-stu-id="8801a-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="8801a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8801a-110">PARAMETERS</span></span>

### <span data-ttu-id="8801a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8801a-111">-DefaultProfile</span></span>
<span data-ttu-id="8801a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8801a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8801a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8801a-113">CommonParameters</span></span>
<span data-ttu-id="8801a-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8801a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8801a-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8801a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8801a-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8801a-116">INPUTS</span></span>

### <span data-ttu-id="8801a-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8801a-117">None</span></span>

## <span data-ttu-id="8801a-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8801a-118">OUTPUTS</span></span>

### <span data-ttu-id="8801a-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="8801a-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="8801a-120">Note</span><span class="sxs-lookup"><span data-stu-id="8801a-120">NOTES</span></span>

## <span data-ttu-id="8801a-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8801a-121">RELATED LINKS</span></span>
