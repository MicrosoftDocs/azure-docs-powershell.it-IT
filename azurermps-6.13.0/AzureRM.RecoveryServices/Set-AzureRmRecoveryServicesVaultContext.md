---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 0989bdcc14a9f7e3cbd65af11aea843cdd0ec6e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509136"
---
# <span data-ttu-id="db512-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="db512-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="db512-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db512-102">SYNOPSIS</span></span>
<span data-ttu-id="db512-103">Imposta il contesto del Vault.</span><span class="sxs-lookup"><span data-stu-id="db512-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db512-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db512-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db512-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db512-105">DESCRIPTION</span></span>
<span data-ttu-id="db512-106">Il cmdlet **set-AzureRmRecoveryServicesVaultContext** imposta il contesto del Vault per i servizi di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="db512-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="db512-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db512-107">EXAMPLES</span></span>

### <span data-ttu-id="db512-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db512-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="db512-109">Imposta il contesto del Vault.</span><span class="sxs-lookup"><span data-stu-id="db512-109">Sets vault context.</span></span>

## <span data-ttu-id="db512-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db512-110">PARAMETERS</span></span>

### <span data-ttu-id="db512-111">-Vault</span><span class="sxs-lookup"><span data-stu-id="db512-111">-Vault</span></span>
<span data-ttu-id="db512-112">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="db512-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="db512-113">Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="db512-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db512-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db512-114">-DefaultProfile</span></span>
<span data-ttu-id="db512-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db512-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db512-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db512-116">CommonParameters</span></span>
<span data-ttu-id="db512-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db512-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db512-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db512-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db512-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db512-119">INPUTS</span></span>

### <span data-ttu-id="db512-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="db512-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="db512-121">Parameters: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db512-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="db512-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db512-122">OUTPUTS</span></span>

### <span data-ttu-id="db512-123">System. void</span><span class="sxs-lookup"><span data-stu-id="db512-123">System.Void</span></span>

## <span data-ttu-id="db512-124">Note</span><span class="sxs-lookup"><span data-stu-id="db512-124">NOTES</span></span>

## <span data-ttu-id="db512-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db512-125">RELATED LINKS</span></span>
