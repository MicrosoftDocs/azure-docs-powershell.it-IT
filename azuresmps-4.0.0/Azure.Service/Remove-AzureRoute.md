---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 5C8A79D1-32D4-4B30-AAC8-C6EF3B68017E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c2f695022e3a03d90443ad9ac2eb36ef8cb22ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029597"
---
# <span data-ttu-id="1222c-101">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="1222c-101">Remove-AzureRoute</span></span>

## <span data-ttu-id="1222c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1222c-102">SYNOPSIS</span></span>
<span data-ttu-id="1222c-103">Consente di rimuovere una route da una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="1222c-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="1222c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1222c-104">SYNTAX</span></span>

```
Remove-AzureRoute -RouteName <String> [-Force] -RouteTable <IRouteTable> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1222c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1222c-105">DESCRIPTION</span></span>
<span data-ttu-id="1222c-106">Il cmdlet **Remove-AzureRoute** consente di rimuovere una route da una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="1222c-106">The **Remove-AzureRoute** cmdlet removes a route from a route table.</span></span>

## <span data-ttu-id="1222c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1222c-107">EXAMPLES</span></span>

### <span data-ttu-id="1222c-108">Esempio 1: rimuovere una route</span><span class="sxs-lookup"><span data-stu-id="1222c-108">Example 1: Remove a route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Remove-AzureRoute -RouteName "InternetRoute"
Confirm
Are you sure you want to remove the Route "InternetRoute" from Route Table "ApplianceRouteTable"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="1222c-109">Questo comando consente di ottenere una tabella di route denominata ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="1222c-109">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="1222c-110">Il comando passa la tabella route al cmdlet Current.</span><span class="sxs-lookup"><span data-stu-id="1222c-110">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="1222c-111">Il cmdlet corrente consente di rimuovere una route denominata InternetRoute.</span><span class="sxs-lookup"><span data-stu-id="1222c-111">The current cmdlet removes a route named InternetRoute.</span></span>

## <span data-ttu-id="1222c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1222c-112">PARAMETERS</span></span>

### <span data-ttu-id="1222c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1222c-113">-Force</span></span>
<span data-ttu-id="1222c-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1222c-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1222c-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="1222c-115">-Profile</span></span>
<span data-ttu-id="1222c-116">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1222c-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1222c-117">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1222c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1222c-118">-RouteName</span><span class="sxs-lookup"><span data-stu-id="1222c-118">-RouteName</span></span>
<span data-ttu-id="1222c-119">Specifica un nome per la nuova route rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1222c-119">Specifies a name for the new route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1222c-120">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1222c-120">-RouteTable</span></span>
<span data-ttu-id="1222c-121">Specifica la tabella di route da cui questo cmdlet rimuove una route.</span><span class="sxs-lookup"><span data-stu-id="1222c-121">Specifies the route table from which this cmdlet removes a route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1222c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1222c-122">CommonParameters</span></span>
<span data-ttu-id="1222c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1222c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1222c-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1222c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1222c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1222c-125">INPUTS</span></span>

## <span data-ttu-id="1222c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1222c-126">OUTPUTS</span></span>

## <span data-ttu-id="1222c-127">Note</span><span class="sxs-lookup"><span data-stu-id="1222c-127">NOTES</span></span>

## <span data-ttu-id="1222c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1222c-128">RELATED LINKS</span></span>

[<span data-ttu-id="1222c-129">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="1222c-129">Set-AzureRoute</span></span>](./Set-AzureRoute.md)


