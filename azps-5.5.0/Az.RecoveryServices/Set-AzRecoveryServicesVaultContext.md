---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191294"
---
# <span data-ttu-id="60d68-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="60d68-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="60d68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60d68-102">SYNOPSIS</span></span>

<span data-ttu-id="60d68-103">Imposta il contesto del vault.</span><span class="sxs-lookup"><span data-stu-id="60d68-103">Sets vault context.</span></span>

## <span data-ttu-id="60d68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60d68-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60d68-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60d68-105">DESCRIPTION</span></span>

<span data-ttu-id="60d68-106">Il cmdlet **Set-AzRecoveryServicesVaultContext** imposta il contesto del vault per i servizi di Ripristino siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="60d68-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="60d68-107">Avviso: questo cmdlet è in fase di deprecazione in un futuro rilascio delle modifiche di interruzione.</span><span class="sxs-lookup"><span data-stu-id="60d68-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="60d68-108">Non ci saranno sostituzioni.</span><span class="sxs-lookup"><span data-stu-id="60d68-108">There will be no replacement for it.</span></span> <span data-ttu-id="60d68-109">Usare il parametro -VaultId in tutti i comandi dei servizi di ripristino in futuro.</span><span class="sxs-lookup"><span data-stu-id="60d68-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="60d68-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60d68-110">EXAMPLES</span></span>

### <span data-ttu-id="60d68-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60d68-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="60d68-112">Imposta il contesto del vault.</span><span class="sxs-lookup"><span data-stu-id="60d68-112">Sets vault context.</span></span>

## <span data-ttu-id="60d68-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60d68-113">PARAMETERS</span></span>

### <span data-ttu-id="60d68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60d68-114">-DefaultProfile</span></span>

<span data-ttu-id="60d68-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60d68-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60d68-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="60d68-116">-Vault</span></span>

<span data-ttu-id="60d68-117">Specifica il nome del vault.</span><span class="sxs-lookup"><span data-stu-id="60d68-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="60d68-118">Il vault deve essere un **oggetto AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="60d68-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="60d68-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60d68-119">CommonParameters</span></span>
<span data-ttu-id="60d68-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60d68-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60d68-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60d68-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60d68-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="60d68-122">INPUTS</span></span>

### <span data-ttu-id="60d68-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="60d68-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="60d68-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60d68-124">OUTPUTS</span></span>

### <span data-ttu-id="60d68-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="60d68-125">System.Void</span></span>

## <span data-ttu-id="60d68-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="60d68-126">NOTES</span></span>

## <span data-ttu-id="60d68-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60d68-127">RELATED LINKS</span></span>
