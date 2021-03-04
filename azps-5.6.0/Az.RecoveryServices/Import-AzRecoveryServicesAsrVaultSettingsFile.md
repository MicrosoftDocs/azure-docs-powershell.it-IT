---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: b287e69093ca748d02cd3f630e3b38fb51cdf8f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007677"
---
# <span data-ttu-id="9e144-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9e144-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="9e144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e144-102">SYNOPSIS</span></span>
<span data-ttu-id="9e144-103">Importa il file di impostazioni del vault ASR specificato per impostare il contesto del vault (contesto della sessione di PowerShell) per le successive operazioni di AsR nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9e144-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="9e144-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e144-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e144-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9e144-105">DESCRIPTION</span></span>
<span data-ttu-id="9e144-106">Il cmdlet **Import-AzRecoveryServicesAsrVaultSettingsFile** importa il file di impostazioni del vault di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="9e144-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="9e144-107">Il file di impostazioni del vault viene usato per impostare il contesto del vault per le successive operazioni di Ripristino siti di Azure nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="9e144-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="9e144-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e144-108">EXAMPLES</span></span>

### <span data-ttu-id="9e144-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e144-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="9e144-110">Importa il file di impostazioni del vault dei servizi di recupero specificato e restituisce le impostazioni del vault importato.</span><span class="sxs-lookup"><span data-stu-id="9e144-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="9e144-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e144-111">PARAMETERS</span></span>

### <span data-ttu-id="9e144-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e144-112">-DefaultProfile</span></span>
<span data-ttu-id="9e144-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e144-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9e144-114">-Path</span><span class="sxs-lookup"><span data-stu-id="9e144-114">-Path</span></span>
<span data-ttu-id="9e144-115">Specifica il percorso della cartella del file di impostazioni del vault ASR.</span><span class="sxs-lookup"><span data-stu-id="9e144-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="9e144-116">Questo file può essere scaricato dal portale del vault dei servizi di ripristino e archiviato in locale.</span><span class="sxs-lookup"><span data-stu-id="9e144-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e144-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e144-117">-Confirm</span></span>
<span data-ttu-id="9e144-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e144-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e144-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e144-119">-WhatIf</span></span>
<span data-ttu-id="9e144-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e144-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e144-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e144-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e144-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e144-122">CommonParameters</span></span>
<span data-ttu-id="9e144-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e144-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e144-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e144-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e144-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="9e144-125">INPUTS</span></span>

### <span data-ttu-id="9e144-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9e144-126">System.String</span></span>

## <span data-ttu-id="9e144-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e144-127">OUTPUTS</span></span>

### <span data-ttu-id="9e144-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="9e144-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="9e144-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="9e144-129">NOTES</span></span>

## <span data-ttu-id="9e144-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e144-130">RELATED LINKS</span></span>

[<span data-ttu-id="9e144-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9e144-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
