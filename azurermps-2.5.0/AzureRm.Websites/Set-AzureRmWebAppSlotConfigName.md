---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
ms.openlocfilehash: 39c3ce693a1ee17a5b547c027ab9165388fe10f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866620"
---
# <span data-ttu-id="69336-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="69336-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="69336-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69336-102">SYNOPSIS</span></span>
<span data-ttu-id="69336-103">Impostare i nomi di configurazione degli slot Web App</span><span class="sxs-lookup"><span data-stu-id="69336-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69336-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69336-104">SYNTAX</span></span>

### <span data-ttu-id="69336-105">S1</span><span class="sxs-lookup"><span data-stu-id="69336-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69336-106">S2</span><span class="sxs-lookup"><span data-stu-id="69336-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69336-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69336-107">DESCRIPTION</span></span>
<span data-ttu-id="69336-108">Il cmdlet **set-AzureRmWebAppSlotConfigName** contrassegna le impostazioni delle app e le stringhe di connessione come impostazioni degli slot</span><span class="sxs-lookup"><span data-stu-id="69336-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="69336-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69336-109">EXAMPLES</span></span>

### <span data-ttu-id="69336-110">1:</span><span class="sxs-lookup"><span data-stu-id="69336-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="69336-111">Questo comando rimuove tutte le impostazioni delle app e le stringhe di connessione per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="69336-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="69336-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69336-112">PARAMETERS</span></span>

### <span data-ttu-id="69336-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="69336-113">-AppSettingNames</span></span>
<span data-ttu-id="69336-114">Matrice di stringhe dei nomi delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="69336-114">App Settings Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69336-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="69336-115">-ConnectionStringNames</span></span>
<span data-ttu-id="69336-116">Stringa di connessione names array</span><span class="sxs-lookup"><span data-stu-id="69336-116">Connection String Names String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69336-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69336-117">-DefaultProfile</span></span>
<span data-ttu-id="69336-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69336-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69336-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="69336-119">-Name</span></span>
<span data-ttu-id="69336-120">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="69336-120">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69336-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="69336-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="69336-122">Opzione Rimuovi tutti i nomi delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="69336-122">Remove All App Setting Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69336-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="69336-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="69336-124">Opzione Rimuovi tutti i nomi delle stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="69336-124">Remove All Connection String Names Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69336-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69336-125">-ResourceGroupName</span></span>
<span data-ttu-id="69336-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="69336-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69336-127">-Web App</span><span class="sxs-lookup"><span data-stu-id="69336-127">-WebApp</span></span>
<span data-ttu-id="69336-128">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="69336-128">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69336-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69336-129">CommonParameters</span></span>
<span data-ttu-id="69336-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69336-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69336-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69336-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69336-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69336-132">INPUTS</span></span>

### <span data-ttu-id="69336-133">Sito</span><span class="sxs-lookup"><span data-stu-id="69336-133">Site</span></span>
<span data-ttu-id="69336-134">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="69336-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="69336-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69336-135">OUTPUTS</span></span>

## <span data-ttu-id="69336-136">Note</span><span class="sxs-lookup"><span data-stu-id="69336-136">NOTES</span></span>

## <span data-ttu-id="69336-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69336-137">RELATED LINKS</span></span>

