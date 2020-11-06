---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/import-azurermrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ef92265a59271e321f9e2002e75cb4ea9d64542d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518051"
---
# <span data-ttu-id="c9890-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c9890-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="c9890-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9890-102">SYNOPSIS</span></span>
<span data-ttu-id="c9890-103">Importa il file di impostazioni di ASR specificato per impostare il contesto del Vault (contesto sessione di PowerShell) per le successive operazioni ASR nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c9890-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9890-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9890-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9890-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9890-105">DESCRIPTION</span></span>
<span data-ttu-id="c9890-106">Il cmdlet **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** importa il file di impostazioni del caveau di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="c9890-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="c9890-107">Il file di impostazioni del Vault viene usato per impostare il contesto del Vault per le successive operazioni di ripristino dei siti di Azure nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="c9890-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="c9890-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9890-108">EXAMPLES</span></span>

### <span data-ttu-id="c9890-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9890-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="c9890-110">Importa il file di impostazioni del Vault di servizi di ripristino specificato e restituisce le impostazioni della volta importato.</span><span class="sxs-lookup"><span data-stu-id="c9890-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="c9890-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9890-111">PARAMETERS</span></span>

### <span data-ttu-id="c9890-112">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c9890-112">-Confirm</span></span>
<span data-ttu-id="c9890-113">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9890-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9890-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9890-114">-DefaultProfile</span></span>
<span data-ttu-id="c9890-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9890-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="c9890-116">-Path</span><span class="sxs-lookup"><span data-stu-id="c9890-116">-Path</span></span>
<span data-ttu-id="c9890-117">Specifica il percorso della cartella del file di impostazioni del Vault ASR.</span><span class="sxs-lookup"><span data-stu-id="c9890-117">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="c9890-118">Questo file può essere scaricato dal portale del Vault di servizi di ripristino e archiviato localmente.</span><span class="sxs-lookup"><span data-stu-id="c9890-118">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9890-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9890-119">-WhatIf</span></span>
<span data-ttu-id="c9890-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9890-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9890-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9890-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9890-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9890-122">CommonParameters</span></span>
<span data-ttu-id="c9890-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9890-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9890-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9890-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9890-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9890-125">INPUTS</span></span>

### <span data-ttu-id="c9890-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c9890-126">System.String</span></span>

## <span data-ttu-id="c9890-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9890-127">OUTPUTS</span></span>

### <span data-ttu-id="c9890-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c9890-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="c9890-129">Note</span><span class="sxs-lookup"><span data-stu-id="c9890-129">NOTES</span></span>

## <span data-ttu-id="c9890-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9890-130">RELATED LINKS</span></span>

[<span data-ttu-id="c9890-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="c9890-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
