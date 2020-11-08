---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029721"
---
# <span data-ttu-id="8b63d-101">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="8b63d-101">Import-AzureStorSimpleLegacyApplianceConfig</span></span>

## <span data-ttu-id="8b63d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b63d-102">SYNOPSIS</span></span>
<span data-ttu-id="8b63d-103">Importa un file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="8b63d-103">Imports a configuration file.</span></span>

## <span data-ttu-id="8b63d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b63d-104">SYNTAX</span></span>

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8b63d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b63d-105">DESCRIPTION</span></span>
<span data-ttu-id="8b63d-106">Il cmdlet **Import-AzureStorSimpleLegacyApplianceConfig** importa il file di configurazione dall'appliance legacy.</span><span class="sxs-lookup"><span data-stu-id="8b63d-106">The **Import-AzureStorSimpleLegacyApplianceConfig** cmdlet imports the configuration file from the legacy appliance.</span></span>
<span data-ttu-id="8b63d-107">Il file contiene informazioni sui contenitori di volumi, i criteri di backup e le credenziali dell'account di archiviazione per il servizio Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="8b63d-107">That file contains information about volume containers, backup policies, and storage account credentials for the Azure StorSimple service.</span></span>
<span data-ttu-id="8b63d-108">Questo cmdlet restituisce i metadati della configurazione degli elettrodomestici legacy.</span><span class="sxs-lookup"><span data-stu-id="8b63d-108">This cmdlet returns the legacy appliance configuration metadata.</span></span>

## <span data-ttu-id="8b63d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b63d-109">EXAMPLES</span></span>

### <span data-ttu-id="8b63d-110">Esempio 1: importare un file di configurazione</span><span class="sxs-lookup"><span data-stu-id="8b63d-110">Example 1: Import a configuration file</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

<span data-ttu-id="8b63d-111">Questo comando importa il file di configurazione nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="8b63d-111">This command imports the configuration file at the specified path.</span></span>
<span data-ttu-id="8b63d-112">Il comando include la chiave per decrittografare il file.</span><span class="sxs-lookup"><span data-stu-id="8b63d-112">The command includes the key to decrypt the file.</span></span>

## <span data-ttu-id="8b63d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b63d-113">PARAMETERS</span></span>

### <span data-ttu-id="8b63d-114">-ConfigDecryptionKey</span><span class="sxs-lookup"><span data-stu-id="8b63d-114">-ConfigDecryptionKey</span></span>
<span data-ttu-id="8b63d-115">Specifica la chiave di decrittografia per la configurazione dell'appliance legacy.</span><span class="sxs-lookup"><span data-stu-id="8b63d-115">Specifies the decryption key for the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b63d-116">-ConfigFilePath</span><span class="sxs-lookup"><span data-stu-id="8b63d-116">-ConfigFilePath</span></span>
<span data-ttu-id="8b63d-117">Specifica il percorso assoluto del file di configurazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="8b63d-117">Specifies the absolute path of the configuration file to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b63d-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="8b63d-118">-Profile</span></span>
<span data-ttu-id="8b63d-119">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="8b63d-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="8b63d-120">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="8b63d-120">-TargetDeviceName</span></span>
<span data-ttu-id="8b63d-121">Specifica il nome del dispositivo di destinazione presentato nel portale.</span><span class="sxs-lookup"><span data-stu-id="8b63d-121">Specifies the name of the target device as presented in the portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b63d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b63d-122">CommonParameters</span></span>
<span data-ttu-id="8b63d-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b63d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b63d-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b63d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b63d-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b63d-125">INPUTS</span></span>

### <span data-ttu-id="8b63d-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8b63d-126">None</span></span>

## <span data-ttu-id="8b63d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b63d-127">OUTPUTS</span></span>

### <span data-ttu-id="8b63d-128">LegacyApplianceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b63d-128">LegacyApplianceConfiguration</span></span>
<span data-ttu-id="8b63d-129">Questo cmdlet restituisce i dettagli della configurazione.</span><span class="sxs-lookup"><span data-stu-id="8b63d-129">This cmdlet returns the details of the configuration.</span></span>
<span data-ttu-id="8b63d-130">L'oggetto **LegacyApplianceConfiguration** contiene le informazioni seguenti: ID configurazione, nomi contenitori volume, record controllo accessi, criteri di backup, impostazioni larghezza di banda, contenitori volume, credenziali account di archiviazione e volumi.</span><span class="sxs-lookup"><span data-stu-id="8b63d-130">The **LegacyApplianceConfiguration** object contains the following information: configuration ID, volume container names, access control records, backup policies, bandwidth settings, volume containers, storage account credentials, and volumes.</span></span>

## <span data-ttu-id="8b63d-131">Note</span><span class="sxs-lookup"><span data-stu-id="8b63d-131">NOTES</span></span>

## <span data-ttu-id="8b63d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b63d-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b63d-133">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8b63d-133">Import-AzureStorSimpleLegacyVolumeContainer</span></span>](./Import-AzureStorSimpleLegacyVolumeContainer.md)


