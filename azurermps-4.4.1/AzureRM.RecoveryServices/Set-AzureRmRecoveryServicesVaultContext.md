---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: d8743b12757d5845107d6a38689059b90bf1e287
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687712"
---
# <span data-ttu-id="69dab-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="69dab-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="69dab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69dab-102">SYNOPSIS</span></span>
<span data-ttu-id="69dab-103">Imposta il contesto del Vault.</span><span class="sxs-lookup"><span data-stu-id="69dab-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69dab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69dab-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69dab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69dab-105">DESCRIPTION</span></span>
<span data-ttu-id="69dab-106">Il cmdlet **set-AzureRmRecoveryServicesVaultContext** imposta il contesto del Vault per i servizi di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="69dab-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="69dab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69dab-107">EXAMPLES</span></span>

## <span data-ttu-id="69dab-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69dab-108">PARAMETERS</span></span>

### <span data-ttu-id="69dab-109">-Vault</span><span class="sxs-lookup"><span data-stu-id="69dab-109">-Vault</span></span>
<span data-ttu-id="69dab-110">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="69dab-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="69dab-111">Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="69dab-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="69dab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69dab-112">-DefaultProfile</span></span>
<span data-ttu-id="69dab-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69dab-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69dab-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69dab-114">CommonParameters</span></span>
<span data-ttu-id="69dab-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69dab-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69dab-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69dab-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69dab-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69dab-117">INPUTS</span></span>

### <span data-ttu-id="69dab-118">ARSVault</span><span class="sxs-lookup"><span data-stu-id="69dab-118">ARSVault</span></span>
<span data-ttu-id="69dab-119">Il parametro "Vault" accetta il valore di tipo "ARSVault" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="69dab-119">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="69dab-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69dab-120">OUTPUTS</span></span>

## <span data-ttu-id="69dab-121">Note</span><span class="sxs-lookup"><span data-stu-id="69dab-121">NOTES</span></span>

## <span data-ttu-id="69dab-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69dab-122">RELATED LINKS</span></span>

