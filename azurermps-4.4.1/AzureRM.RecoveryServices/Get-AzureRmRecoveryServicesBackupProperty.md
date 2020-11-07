---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 3e93df0adfe1e1bc10d5ea74dd189bee60595824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687104"
---
# <span data-ttu-id="80a76-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="80a76-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="80a76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80a76-102">SYNOPSIS</span></span>
<span data-ttu-id="80a76-103">Ottiene le proprietà di backup.</span><span class="sxs-lookup"><span data-stu-id="80a76-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80a76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80a76-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80a76-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80a76-105">DESCRIPTION</span></span>
<span data-ttu-id="80a76-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupProperty** ottiene le proprietà di backup per un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="80a76-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="80a76-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80a76-107">EXAMPLES</span></span>

## <span data-ttu-id="80a76-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80a76-108">PARAMETERS</span></span>

### <span data-ttu-id="80a76-109">-Vault</span><span class="sxs-lookup"><span data-stu-id="80a76-109">-Vault</span></span>
<span data-ttu-id="80a76-110">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="80a76-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="80a76-111">Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="80a76-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80a76-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a76-112">-DefaultProfile</span></span>
<span data-ttu-id="80a76-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80a76-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80a76-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a76-114">CommonParameters</span></span>
<span data-ttu-id="80a76-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a76-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a76-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a76-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a76-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80a76-117">INPUTS</span></span>

### <span data-ttu-id="80a76-118">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="80a76-118">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="80a76-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80a76-119">OUTPUTS</span></span>

### <span data-ttu-id="80a76-120">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="80a76-120">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="80a76-121">Note</span><span class="sxs-lookup"><span data-stu-id="80a76-121">NOTES</span></span>

## <span data-ttu-id="80a76-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80a76-122">RELATED LINKS</span></span>

