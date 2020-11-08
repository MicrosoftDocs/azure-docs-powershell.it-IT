---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlotConfigName.md
ms.openlocfilehash: a2c57ebe6f85209596628dffe9de88ca260bbafa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020557"
---
# <span data-ttu-id="117bb-101">Set-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="117bb-101">Set-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="117bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="117bb-102">SYNOPSIS</span></span>
<span data-ttu-id="117bb-103">Impostare i nomi di configurazione degli slot Web App</span><span class="sxs-lookup"><span data-stu-id="117bb-103">Set Web App Slot Config names</span></span>

## <span data-ttu-id="117bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="117bb-104">SYNTAX</span></span>

### <span data-ttu-id="117bb-105">S1</span><span class="sxs-lookup"><span data-stu-id="117bb-105">S1</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="117bb-106">S2</span><span class="sxs-lookup"><span data-stu-id="117bb-106">S2</span></span>
```
Set-AzWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="117bb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="117bb-107">DESCRIPTION</span></span>
<span data-ttu-id="117bb-108">Il cmdlet **set-AzWebAppSlotConfigName** contrassegna le impostazioni delle app e le stringhe di connessione come impostazioni degli slot</span><span class="sxs-lookup"><span data-stu-id="117bb-108">The **Set-AzWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="117bb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="117bb-109">EXAMPLES</span></span>

### <span data-ttu-id="117bb-110">1:</span><span class="sxs-lookup"><span data-stu-id="117bb-110">1:</span></span>
```
PS C:\> Set-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="117bb-111">Questo comando rimuove tutte le impostazioni delle app e le stringhe di connessione per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="117bb-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="117bb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="117bb-112">PARAMETERS</span></span>

### <span data-ttu-id="117bb-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="117bb-113">-AppSettingNames</span></span>
<span data-ttu-id="117bb-114">Matrice di stringhe dei nomi delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="117bb-114">App Settings Names String Array</span></span>

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

### <span data-ttu-id="117bb-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="117bb-115">-ConnectionStringNames</span></span>
<span data-ttu-id="117bb-116">Stringa di connessione names array</span><span class="sxs-lookup"><span data-stu-id="117bb-116">Connection String Names String Array</span></span>

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

### <span data-ttu-id="117bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117bb-117">-DefaultProfile</span></span>
<span data-ttu-id="117bb-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="117bb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="117bb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="117bb-119">-Name</span></span>
<span data-ttu-id="117bb-120">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="117bb-120">WebApp Name</span></span>

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

### <span data-ttu-id="117bb-121">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="117bb-121">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="117bb-122">Opzione Rimuovi tutti i nomi delle impostazioni dell'app</span><span class="sxs-lookup"><span data-stu-id="117bb-122">Remove All App Setting Names Option</span></span>

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

### <span data-ttu-id="117bb-123">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="117bb-123">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="117bb-124">Opzione Rimuovi tutti i nomi delle stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="117bb-124">Remove All Connection String Names Option</span></span>

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

### <span data-ttu-id="117bb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="117bb-125">-ResourceGroupName</span></span>
<span data-ttu-id="117bb-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="117bb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="117bb-127">-Web App</span><span class="sxs-lookup"><span data-stu-id="117bb-127">-WebApp</span></span>
<span data-ttu-id="117bb-128">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="117bb-128">WebApp Object</span></span>

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

### <span data-ttu-id="117bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117bb-129">CommonParameters</span></span>
<span data-ttu-id="117bb-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="117bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117bb-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117bb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117bb-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="117bb-132">INPUTS</span></span>

### <span data-ttu-id="117bb-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="117bb-133">System.String[]</span></span>

### <span data-ttu-id="117bb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="117bb-134">System.String</span></span>

### <span data-ttu-id="117bb-135">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="117bb-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="117bb-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="117bb-136">OUTPUTS</span></span>

### <span data-ttu-id="117bb-137">Microsoft. Azure. Management. website. Models. SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="117bb-137">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="117bb-138">Note</span><span class="sxs-lookup"><span data-stu-id="117bb-138">NOTES</span></span>

## <span data-ttu-id="117bb-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="117bb-139">RELATED LINKS</span></span>
