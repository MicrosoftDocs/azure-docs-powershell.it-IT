---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 75c134b162636f94b00cf6692f4e9df120930dcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516291"
---
# <span data-ttu-id="243b4-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="243b4-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="243b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="243b4-102">SYNOPSIS</span></span>
<span data-ttu-id="243b4-103">Impostare i nomi di configurazione degli slot Web App</span><span class="sxs-lookup"><span data-stu-id="243b4-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="243b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="243b4-104">SYNTAX</span></span>

### <span data-ttu-id="243b4-105">S1</span><span class="sxs-lookup"><span data-stu-id="243b4-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="243b4-106">S2</span><span class="sxs-lookup"><span data-stu-id="243b4-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="243b4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="243b4-107">DESCRIPTION</span></span>
<span data-ttu-id="243b4-108">Il cmdlet **set-AzureRmWebAppSlotConfigName** contrassegna le impostazioni delle app e le stringhe di connessione come impostazioni degli slot</span><span class="sxs-lookup"><span data-stu-id="243b4-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="243b4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="243b4-109">EXAMPLES</span></span>

### <span data-ttu-id="243b4-110">1:</span><span class="sxs-lookup"><span data-stu-id="243b4-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="243b4-111">Questo comando rimuove tutte le impostazioni delle app e le stringhe di connessione per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="243b4-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="243b4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="243b4-112">PARAMETERS</span></span>

### <span data-ttu-id="243b4-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="243b4-113">-AppSettingNames</span></span>
<span data-ttu-id="243b4-114">Matrice di stringhe dei nomi delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="243b4-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="243b4-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="243b4-115">-ConnectionStringNames</span></span>
<span data-ttu-id="243b4-116">Stringa di connessione names array</span><span class="sxs-lookup"><span data-stu-id="243b4-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="243b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="243b4-117">-DefaultProfile</span></span>
<span data-ttu-id="243b4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="243b4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="243b4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="243b4-119">-Name</span></span>
<span data-ttu-id="243b4-120">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="243b4-120">WebApp Name</span></span>

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

### <span data-ttu-id="243b4-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="243b4-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="243b4-122">Opzione Rimuovi tutti i nomi delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="243b4-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="243b4-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="243b4-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="243b4-124">Opzione Rimuovi tutti i nomi delle stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="243b4-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="243b4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="243b4-125">-ResourceGroupName</span></span>
<span data-ttu-id="243b4-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="243b4-126">Resource Group Name</span></span>

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

### <span data-ttu-id="243b4-127">-Web App</span><span class="sxs-lookup"><span data-stu-id="243b4-127">-WebApp</span></span>
<span data-ttu-id="243b4-128">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="243b4-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="243b4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="243b4-129">CommonParameters</span></span>
<span data-ttu-id="243b4-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="243b4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="243b4-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="243b4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="243b4-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="243b4-132">INPUTS</span></span>

### <span data-ttu-id="243b4-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="243b4-133">System.String[]</span></span>

### <span data-ttu-id="243b4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="243b4-134">System.String</span></span>

### <span data-ttu-id="243b4-135">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="243b4-135">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="243b4-136">Parametri: Web App (ByValue)</span><span class="sxs-lookup"><span data-stu-id="243b4-136">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="243b4-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="243b4-137">OUTPUTS</span></span>

### <span data-ttu-id="243b4-138">Microsoft. Azure. Management. website. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="243b4-138">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="243b4-139">Note</span><span class="sxs-lookup"><span data-stu-id="243b4-139">NOTES</span></span>

## <span data-ttu-id="243b4-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="243b4-140">RELATED LINKS</span></span>