---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030026"
---
# <span data-ttu-id="8c271-101">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8c271-101">Get-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="8c271-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c271-102">SYNOPSIS</span></span>
<span data-ttu-id="8c271-103">Ottiene il file di impostazioni del caveau di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="8c271-103">Gets the Site Recovery vault settings file.</span></span>

## <span data-ttu-id="8c271-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c271-104">SYNTAX</span></span>

### <span data-ttu-id="8c271-105">ByParam (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c271-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8c271-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="8c271-106">ByObject</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c271-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c271-107">DESCRIPTION</span></span>
<span data-ttu-id="8c271-108">Il cmdlet **Get-AzureSiteRecoveryVaultSettingsFile** ottiene il file di impostazioni per un Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="8c271-108">The **Get-AzureSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="8c271-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c271-109">EXAMPLES</span></span>

### <span data-ttu-id="8c271-110">Esempio 1: recuperare il file di impostazioni per un Vault</span><span class="sxs-lookup"><span data-stu-id="8c271-110">Example 1: Get the settings file for a vault</span></span>
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

<span data-ttu-id="8c271-111">Il primo comando ottiene il Vault di ripristino del sito di Azure attivo denominato ContosoVault usando il cmdlet **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="8c271-111">The first command gets the active Azure Site Recovery vault named ContosoVault by using the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>
<span data-ttu-id="8c271-112">Il comando Archivia il Vault nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="8c271-112">The command stores that vault in the $Vault variable.</span></span>

<span data-ttu-id="8c271-113">Il secondo comando ottiene il file di impostazioni per il Vault archiviato in $Vault.</span><span class="sxs-lookup"><span data-stu-id="8c271-113">The second command gets the settings file for the vault stored in $Vault.</span></span>

## <span data-ttu-id="8c271-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c271-114">PARAMETERS</span></span>

### <span data-ttu-id="8c271-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8c271-115">-Location</span></span>
<span data-ttu-id="8c271-116">Specifica la posizione geografica a cui appartiene il Vault.</span><span class="sxs-lookup"><span data-stu-id="8c271-116">Specifies the geographical location to which the vault belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c271-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c271-117">-Name</span></span>
<span data-ttu-id="8c271-118">Specifica il nome di un Vault.</span><span class="sxs-lookup"><span data-stu-id="8c271-118">Specifies the name of a vault.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c271-119">-Path</span><span class="sxs-lookup"><span data-stu-id="8c271-119">-Path</span></span>
<span data-ttu-id="8c271-120">Specifica il percorso del file di impostazioni del caveau di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="8c271-120">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="8c271-121">Per archiviare il file in locale, scaricarlo dal portale del Vault Recovery del sito dopo che il comando è terminato.</span><span class="sxs-lookup"><span data-stu-id="8c271-121">To store this file locally, download it from the Site Recovery vault portal after the command has finished running.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c271-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="8c271-122">-Profile</span></span>
<span data-ttu-id="8c271-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c271-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c271-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8c271-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c271-125">-Sito</span><span class="sxs-lookup"><span data-stu-id="8c271-125">-Site</span></span>
<span data-ttu-id="8c271-126">Specifica un sito per cui ottenere un file di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="8c271-126">Specifies a site for which to get a settings file.</span></span>
<span data-ttu-id="8c271-127">Per ottenere un oggetto **sito** , usare il cmdlet **Get-AzureSiteRecoverySite** .</span><span class="sxs-lookup"><span data-stu-id="8c271-127">To obtain a **Site** object, use the **Get-AzureSiteRecoverySite** cmdlet.</span></span>

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c271-128">-SiteId</span><span class="sxs-lookup"><span data-stu-id="8c271-128">-SiteId</span></span>
<span data-ttu-id="8c271-129">Specifica l'ID di un sito.</span><span class="sxs-lookup"><span data-stu-id="8c271-129">Specifies the ID of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c271-130">-SiteName</span><span class="sxs-lookup"><span data-stu-id="8c271-130">-SiteName</span></span>
<span data-ttu-id="8c271-131">Specifica il nome di un sito.</span><span class="sxs-lookup"><span data-stu-id="8c271-131">Specifies the name of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c271-132">-Vault</span><span class="sxs-lookup"><span data-stu-id="8c271-132">-Vault</span></span>
<span data-ttu-id="8c271-133">Specifica il Vault per il sito.</span><span class="sxs-lookup"><span data-stu-id="8c271-133">Specifies the vault for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c271-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c271-134">CommonParameters</span></span>
<span data-ttu-id="8c271-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c271-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c271-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c271-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c271-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c271-137">INPUTS</span></span>

## <span data-ttu-id="8c271-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c271-138">OUTPUTS</span></span>

## <span data-ttu-id="8c271-139">Note</span><span class="sxs-lookup"><span data-stu-id="8c271-139">NOTES</span></span>

## <span data-ttu-id="8c271-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c271-140">RELATED LINKS</span></span>

[<span data-ttu-id="8c271-141">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="8c271-141">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)

[<span data-ttu-id="8c271-142">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="8c271-142">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="8c271-143">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="8c271-143">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="8c271-144">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8c271-144">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


