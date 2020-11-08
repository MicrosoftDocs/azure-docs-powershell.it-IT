---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: de3604a4bf1f9c46bf88b2f3cda25982672e9096
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022670"
---
# <span data-ttu-id="0a415-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0a415-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="0a415-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0a415-102">SYNOPSIS</span></span>
<span data-ttu-id="0a415-103">Importa il file di impostazioni di ASR specificato per impostare il contesto del Vault (contesto sessione di PowerShell) per le successive operazioni ASR nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a415-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="0a415-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a415-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a415-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a415-105">DESCRIPTION</span></span>
<span data-ttu-id="0a415-106">Il cmdlet **Import-AzRecoveryServicesAsrVaultSettingsFile** importa il file di impostazioni del caveau di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="0a415-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="0a415-107">Il file di impostazioni del Vault viene usato per impostare il contesto del Vault per le successive operazioni di ripristino dei siti di Azure nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="0a415-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="0a415-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a415-108">EXAMPLES</span></span>

### <span data-ttu-id="0a415-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0a415-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="0a415-110">Importa il file di impostazioni del Vault di servizi di ripristino specificato e restituisce le impostazioni della volta importato.</span><span class="sxs-lookup"><span data-stu-id="0a415-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="0a415-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0a415-111">PARAMETERS</span></span>

### <span data-ttu-id="0a415-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a415-112">-DefaultProfile</span></span>
<span data-ttu-id="0a415-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a415-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0a415-114">-Path</span><span class="sxs-lookup"><span data-stu-id="0a415-114">-Path</span></span>
<span data-ttu-id="0a415-115">Specifica il percorso della cartella del file di impostazioni del Vault ASR.</span><span class="sxs-lookup"><span data-stu-id="0a415-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="0a415-116">Questo file può essere scaricato dal portale del Vault di servizi di ripristino e archiviato localmente.</span><span class="sxs-lookup"><span data-stu-id="0a415-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="0a415-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0a415-117">-Confirm</span></span>
<span data-ttu-id="0a415-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a415-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a415-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a415-119">-WhatIf</span></span>
<span data-ttu-id="0a415-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a415-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a415-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a415-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a415-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a415-122">CommonParameters</span></span>
<span data-ttu-id="0a415-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a415-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a415-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a415-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a415-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0a415-125">INPUTS</span></span>

### <span data-ttu-id="0a415-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0a415-126">System.String</span></span>

## <span data-ttu-id="0a415-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a415-127">OUTPUTS</span></span>

### <span data-ttu-id="0a415-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="0a415-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="0a415-129">Note</span><span class="sxs-lookup"><span data-stu-id="0a415-129">NOTES</span></span>

## <span data-ttu-id="0a415-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a415-130">RELATED LINKS</span></span>

[<span data-ttu-id="0a415-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0a415-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
