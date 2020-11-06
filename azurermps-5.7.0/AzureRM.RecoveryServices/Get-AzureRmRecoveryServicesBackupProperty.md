---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 19e443a4e7bca12a988e3a339fe9d568d81431b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519886"
---
# <span data-ttu-id="4e0a6-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="4e0a6-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="4e0a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0a6-103">Ottiene le proprietà di backup.</span><span class="sxs-lookup"><span data-stu-id="4e0a6-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e0a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e0a6-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e0a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e0a6-105">DESCRIPTION</span></span>
<span data-ttu-id="4e0a6-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupProperty** ottiene le proprietà di backup per un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4e0a6-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="4e0a6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e0a6-107">EXAMPLES</span></span>

### <span data-ttu-id="4e0a6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e0a6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="4e0a6-109">Ottenere la proprietà backup Vault per Vault.</span><span class="sxs-lookup"><span data-stu-id="4e0a6-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="4e0a6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e0a6-110">PARAMETERS</span></span>

### <span data-ttu-id="4e0a6-111">-Vault</span><span class="sxs-lookup"><span data-stu-id="4e0a6-111">-Vault</span></span>
<span data-ttu-id="4e0a6-112">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="4e0a6-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="4e0a6-113">Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="4e0a6-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="4e0a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0a6-114">-DefaultProfile</span></span>
<span data-ttu-id="4e0a6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0a6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e0a6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0a6-116">CommonParameters</span></span>
<span data-ttu-id="4e0a6-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e0a6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0a6-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e0a6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0a6-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e0a6-119">INPUTS</span></span>

### <span data-ttu-id="4e0a6-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="4e0a6-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="4e0a6-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e0a6-121">OUTPUTS</span></span>

### <span data-ttu-id="4e0a6-122">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="4e0a6-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="4e0a6-123">Note</span><span class="sxs-lookup"><span data-stu-id="4e0a6-123">NOTES</span></span>

## <span data-ttu-id="4e0a6-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e0a6-124">RELATED LINKS</span></span>

