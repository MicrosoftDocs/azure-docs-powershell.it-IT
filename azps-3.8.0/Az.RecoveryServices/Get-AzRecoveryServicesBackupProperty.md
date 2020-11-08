---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018842"
---
# <span data-ttu-id="3ba3a-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="3ba3a-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="3ba3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ba3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ba3a-103">Ottiene le proprietà di backup.</span><span class="sxs-lookup"><span data-stu-id="3ba3a-103">Gets Backup properties.</span></span>

## <span data-ttu-id="3ba3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ba3a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ba3a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ba3a-105">DESCRIPTION</span></span>
<span data-ttu-id="3ba3a-106">Il cmdlet **Get-AzRecoveryServicesBackupProperty** ottiene le proprietà di backup per un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="3ba3a-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="3ba3a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ba3a-107">EXAMPLES</span></span>

### <span data-ttu-id="3ba3a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3ba3a-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="3ba3a-109">Ottenere la proprietà backup Vault per Vault.</span><span class="sxs-lookup"><span data-stu-id="3ba3a-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="3ba3a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ba3a-110">PARAMETERS</span></span>

### <span data-ttu-id="3ba3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ba3a-111">-DefaultProfile</span></span>
<span data-ttu-id="3ba3a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3ba3a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ba3a-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="3ba3a-113">-Vault</span></span>
<span data-ttu-id="3ba3a-114">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="3ba3a-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="3ba3a-115">Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="3ba3a-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="3ba3a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ba3a-116">CommonParameters</span></span>
<span data-ttu-id="3ba3a-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ba3a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ba3a-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ba3a-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ba3a-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ba3a-119">INPUTS</span></span>

### <span data-ttu-id="3ba3a-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="3ba3a-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="3ba3a-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ba3a-121">OUTPUTS</span></span>

### <span data-ttu-id="3ba3a-122">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="3ba3a-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="3ba3a-123">Note</span><span class="sxs-lookup"><span data-stu-id="3ba3a-123">NOTES</span></span>

## <span data-ttu-id="3ba3a-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ba3a-124">RELATED LINKS</span></span>
