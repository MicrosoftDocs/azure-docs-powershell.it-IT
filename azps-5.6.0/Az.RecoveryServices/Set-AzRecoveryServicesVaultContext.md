---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 04fa3c9a7024b8a9e1f525a4ef131ae151f25804
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997399"
---
# <span data-ttu-id="75cd8-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="75cd8-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="75cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75cd8-102">SYNOPSIS</span></span>

<span data-ttu-id="75cd8-103">Imposta il contesto del vault.</span><span class="sxs-lookup"><span data-stu-id="75cd8-103">Sets vault context.</span></span>

## <span data-ttu-id="75cd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75cd8-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75cd8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75cd8-105">DESCRIPTION</span></span>

<span data-ttu-id="75cd8-106">Il cmdlet **Set-AzRecoveryServicesVaultContext** imposta il contesto del vault per i servizi di Ripristino siti di Azure.</span><span class="sxs-lookup"><span data-stu-id="75cd8-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="75cd8-107">Avviso: questo cmdlet è in fase di deprecazione in un futuro rilascio delle modifiche di interruzione.</span><span class="sxs-lookup"><span data-stu-id="75cd8-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="75cd8-108">Non ci saranno sostituzioni.</span><span class="sxs-lookup"><span data-stu-id="75cd8-108">There will be no replacement for it.</span></span> <span data-ttu-id="75cd8-109">Usare il parametro -VaultId in tutti i comandi dei servizi di ripristino in futuro.</span><span class="sxs-lookup"><span data-stu-id="75cd8-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="75cd8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75cd8-110">EXAMPLES</span></span>

### <span data-ttu-id="75cd8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75cd8-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="75cd8-112">Imposta il contesto del vault.</span><span class="sxs-lookup"><span data-stu-id="75cd8-112">Sets vault context.</span></span>

## <span data-ttu-id="75cd8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75cd8-113">PARAMETERS</span></span>

### <span data-ttu-id="75cd8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cd8-114">-DefaultProfile</span></span>

<span data-ttu-id="75cd8-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75cd8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75cd8-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="75cd8-116">-Vault</span></span>

<span data-ttu-id="75cd8-117">Specifica il nome del vault.</span><span class="sxs-lookup"><span data-stu-id="75cd8-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="75cd8-118">Il vault deve essere un **oggetto AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="75cd8-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="75cd8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cd8-119">CommonParameters</span></span>
<span data-ttu-id="75cd8-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cd8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cd8-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75cd8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cd8-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="75cd8-122">INPUTS</span></span>

### <span data-ttu-id="75cd8-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="75cd8-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="75cd8-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75cd8-124">OUTPUTS</span></span>

### <span data-ttu-id="75cd8-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="75cd8-125">System.Void</span></span>

## <span data-ttu-id="75cd8-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="75cd8-126">NOTES</span></span>

## <span data-ttu-id="75cd8-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75cd8-127">RELATED LINKS</span></span>
