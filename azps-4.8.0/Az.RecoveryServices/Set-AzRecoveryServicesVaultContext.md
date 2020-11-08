---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191974"
---
# <span data-ttu-id="ee909-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="ee909-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="ee909-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee909-102">SYNOPSIS</span></span>

<span data-ttu-id="ee909-103">Imposta il contesto del Vault.</span><span class="sxs-lookup"><span data-stu-id="ee909-103">Sets vault context.</span></span>

## <span data-ttu-id="ee909-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee909-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee909-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee909-105">DESCRIPTION</span></span>

<span data-ttu-id="ee909-106">Il cmdlet **set-AzRecoveryServicesVaultContext** imposta il contesto del Vault per i servizi di ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="ee909-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="ee909-107">Avviso: questo cmdlet è deprecato in una versione futura per le modifiche alle interruzioni.</span><span class="sxs-lookup"><span data-stu-id="ee909-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="ee909-108">Non saranno disponibili sostituzioni.</span><span class="sxs-lookup"><span data-stu-id="ee909-108">There will be no replacement for it.</span></span> <span data-ttu-id="ee909-109">Usare il parametro-VaultId in tutti i comandi per i servizi di recupero in corso.</span><span class="sxs-lookup"><span data-stu-id="ee909-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="ee909-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee909-110">EXAMPLES</span></span>

### <span data-ttu-id="ee909-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee909-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="ee909-112">Imposta il contesto del Vault.</span><span class="sxs-lookup"><span data-stu-id="ee909-112">Sets vault context.</span></span>

## <span data-ttu-id="ee909-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee909-113">PARAMETERS</span></span>

### <span data-ttu-id="ee909-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee909-114">-DefaultProfile</span></span>

<span data-ttu-id="ee909-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee909-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee909-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="ee909-116">-Vault</span></span>

<span data-ttu-id="ee909-117">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="ee909-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="ee909-118">Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="ee909-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="ee909-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee909-119">CommonParameters</span></span>
<span data-ttu-id="ee909-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee909-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee909-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee909-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee909-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee909-122">INPUTS</span></span>

### <span data-ttu-id="ee909-123">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="ee909-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ee909-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee909-124">OUTPUTS</span></span>

### <span data-ttu-id="ee909-125">System. void</span><span class="sxs-lookup"><span data-stu-id="ee909-125">System.Void</span></span>

## <span data-ttu-id="ee909-126">Note</span><span class="sxs-lookup"><span data-stu-id="ee909-126">NOTES</span></span>

## <span data-ttu-id="ee909-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee909-127">RELATED LINKS</span></span>
