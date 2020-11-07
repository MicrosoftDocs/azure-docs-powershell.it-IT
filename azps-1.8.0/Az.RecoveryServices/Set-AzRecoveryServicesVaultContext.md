---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 4d8839d36bf337e3a710fe31384bb022582a371d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677562"
---
# <span data-ttu-id="2d697-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="2d697-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="2d697-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d697-102">SYNOPSIS</span></span>
<span data-ttu-id="2d697-103">Imposta il contesto del Vault.</span><span class="sxs-lookup"><span data-stu-id="2d697-103">Sets vault context.</span></span>

## <span data-ttu-id="2d697-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d697-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d697-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d697-105">DESCRIPTION</span></span>
<span data-ttu-id="2d697-106">Il cmdlet **set-AzRecoveryServicesVaultContext** imposta il contesto del Vault per i servizi di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="2d697-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="2d697-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d697-107">EXAMPLES</span></span>

### <span data-ttu-id="2d697-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2d697-108">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="2d697-109">Imposta il contesto del Vault.</span><span class="sxs-lookup"><span data-stu-id="2d697-109">Sets vault context.</span></span>

## <span data-ttu-id="2d697-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d697-110">PARAMETERS</span></span>

### <span data-ttu-id="2d697-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d697-111">-DefaultProfile</span></span>
<span data-ttu-id="2d697-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d697-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d697-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="2d697-113">-Vault</span></span>
<span data-ttu-id="2d697-114">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="2d697-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="2d697-115">Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="2d697-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="2d697-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d697-116">CommonParameters</span></span>
<span data-ttu-id="2d697-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d697-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d697-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d697-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d697-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d697-119">INPUTS</span></span>

### <span data-ttu-id="2d697-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="2d697-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="2d697-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d697-121">OUTPUTS</span></span>

### <span data-ttu-id="2d697-122">System. void</span><span class="sxs-lookup"><span data-stu-id="2d697-122">System.Void</span></span>

## <span data-ttu-id="2d697-123">Note</span><span class="sxs-lookup"><span data-stu-id="2d697-123">NOTES</span></span>

## <span data-ttu-id="2d697-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d697-124">RELATED LINKS</span></span>