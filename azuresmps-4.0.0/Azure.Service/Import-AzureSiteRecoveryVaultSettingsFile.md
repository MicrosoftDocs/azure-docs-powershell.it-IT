---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029722"
---
# <span data-ttu-id="67513-101">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="67513-101">Import-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="67513-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67513-102">SYNOPSIS</span></span>
<span data-ttu-id="67513-103">Importa un file di impostazioni del caveau di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="67513-103">Imports a Site Recovery vault settings file.</span></span>

## <span data-ttu-id="67513-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67513-104">SYNTAX</span></span>

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="67513-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67513-105">DESCRIPTION</span></span>
<span data-ttu-id="67513-106">Il cmdlet **Import-AzureSiteRecoveryVaultSettingsFile** importa un file di impostazioni del Vault di ripristino di Azure site per impostare il contesto del Vault per le successive operazioni di ripristino del sito nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="67513-106">The **Import-AzureSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="67513-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67513-107">EXAMPLES</span></span>

### <span data-ttu-id="67513-108">Esempio 1: importare un file di impostazioni del Vault</span><span class="sxs-lookup"><span data-stu-id="67513-108">Example 1: Import a vault settings file</span></span>
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="67513-109">Questo comando importa il file delle impostazioni del Vault nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="67513-109">This command imports the vault settings file at the specified path.</span></span>

## <span data-ttu-id="67513-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67513-110">PARAMETERS</span></span>

### <span data-ttu-id="67513-111">-Path</span><span class="sxs-lookup"><span data-stu-id="67513-111">-Path</span></span>
<span data-ttu-id="67513-112">Specifica il percorso del file di impostazioni del caveau di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="67513-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="67513-113">Questo file può essere scaricato dal portale della volta di ripristino del sito e archiviato localmente.</span><span class="sxs-lookup"><span data-stu-id="67513-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67513-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="67513-114">-Profile</span></span>
<span data-ttu-id="67513-115">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67513-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67513-116">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="67513-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67513-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67513-117">CommonParameters</span></span>
<span data-ttu-id="67513-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67513-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67513-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67513-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67513-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67513-120">INPUTS</span></span>

## <span data-ttu-id="67513-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67513-121">OUTPUTS</span></span>

## <span data-ttu-id="67513-122">Note</span><span class="sxs-lookup"><span data-stu-id="67513-122">NOTES</span></span>

## <span data-ttu-id="67513-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67513-123">RELATED LINKS</span></span>

[<span data-ttu-id="67513-124">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="67513-124">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="67513-125">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="67513-125">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)


