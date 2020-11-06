---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 3ed7bd25c394c2bef5cb3636a4f8c238f45a3558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508483"
---
# <span data-ttu-id="3dead-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="3dead-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="3dead-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dead-102">SYNOPSIS</span></span>
<span data-ttu-id="3dead-103">Impostare i nomi di configurazione degli slot Web App</span><span class="sxs-lookup"><span data-stu-id="3dead-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dead-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dead-104">SYNTAX</span></span>

### <span data-ttu-id="3dead-105">S1</span><span class="sxs-lookup"><span data-stu-id="3dead-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dead-106">S2</span><span class="sxs-lookup"><span data-stu-id="3dead-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dead-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dead-107">DESCRIPTION</span></span>
<span data-ttu-id="3dead-108">Il cmdlet **set-AzureRmWebAppSlotConfigName** contrassegna le impostazioni delle app e le stringhe di connessione come impostazioni degli slot</span><span class="sxs-lookup"><span data-stu-id="3dead-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="3dead-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dead-109">EXAMPLES</span></span>

### <span data-ttu-id="3dead-110">1:</span><span class="sxs-lookup"><span data-stu-id="3dead-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="3dead-111">Questo comando rimuove tutte le impostazioni delle app e le stringhe di connessione per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="3dead-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3dead-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dead-112">PARAMETERS</span></span>

### <span data-ttu-id="3dead-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="3dead-113">-AppSettingNames</span></span>
<span data-ttu-id="3dead-114">Matrice di stringhe dei nomi delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="3dead-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dead-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="3dead-115">-ConnectionStringNames</span></span>
<span data-ttu-id="3dead-116">Stringa di connessione names array</span><span class="sxs-lookup"><span data-stu-id="3dead-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dead-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dead-117">-Name</span></span>
<span data-ttu-id="3dead-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="3dead-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dead-119">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="3dead-119">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="3dead-120">Opzione Rimuovi tutti i nomi delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="3dead-120">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dead-121">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="3dead-121">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="3dead-122">Opzione Rimuovi tutti i nomi delle stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="3dead-122">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dead-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dead-123">-ResourceGroupName</span></span>
<span data-ttu-id="3dead-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3dead-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dead-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="3dead-125">-WebApp</span></span>
<span data-ttu-id="3dead-126">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="3dead-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dead-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dead-127">-DefaultProfile</span></span>
<span data-ttu-id="3dead-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dead-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dead-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dead-129">CommonParameters</span></span>
<span data-ttu-id="3dead-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dead-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dead-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dead-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dead-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dead-132">INPUTS</span></span>

### <span data-ttu-id="3dead-133">Sito</span><span class="sxs-lookup"><span data-stu-id="3dead-133">Site</span></span>
<span data-ttu-id="3dead-134">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3dead-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3dead-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dead-135">OUTPUTS</span></span>

## <span data-ttu-id="3dead-136">Note</span><span class="sxs-lookup"><span data-stu-id="3dead-136">NOTES</span></span>

## <span data-ttu-id="3dead-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dead-137">RELATED LINKS</span></span>

