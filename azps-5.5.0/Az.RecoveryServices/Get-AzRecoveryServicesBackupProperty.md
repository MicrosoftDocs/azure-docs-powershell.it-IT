---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186630"
---
# <span data-ttu-id="c8eaf-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="c8eaf-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="c8eaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="c8eaf-103">Recupera le proprietà di backup.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-103">Gets Backup properties.</span></span>

## <span data-ttu-id="c8eaf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8eaf-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8eaf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c8eaf-105">DESCRIPTION</span></span>
<span data-ttu-id="c8eaf-106">Il cmdlet **Get-AzRecoveryServicesBackupProperty** ottiene le proprietà di backup per un vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="c8eaf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8eaf-107">EXAMPLES</span></span>

### <span data-ttu-id="c8eaf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8eaf-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="c8eaf-109">Ottenere la proprietà del vault di backup per il Vault.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="c8eaf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8eaf-110">PARAMETERS</span></span>

### <span data-ttu-id="c8eaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8eaf-111">-DefaultProfile</span></span>
<span data-ttu-id="c8eaf-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8eaf-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="c8eaf-113">-Vault</span></span>
<span data-ttu-id="c8eaf-114">Specifica il nome del vault.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="c8eaf-115">Il vault deve essere un **oggetto AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="c8eaf-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="c8eaf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8eaf-116">CommonParameters</span></span>
<span data-ttu-id="c8eaf-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8eaf-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c8eaf-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8eaf-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="c8eaf-119">INPUTS</span></span>

### <span data-ttu-id="c8eaf-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="c8eaf-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="c8eaf-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8eaf-121">OUTPUTS</span></span>

### <span data-ttu-id="c8eaf-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="c8eaf-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="c8eaf-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="c8eaf-123">NOTES</span></span>

## <span data-ttu-id="c8eaf-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8eaf-124">RELATED LINKS</span></span>
