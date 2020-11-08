---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7F8C2223-5F82-4E4E-8057-44B72F7D5803
online version: ''
schema: 2.0.0
ms.openlocfilehash: a02d80d46696ff635da95c6bc29875f697f65fd4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029775"
---
# <span data-ttu-id="d77ed-101">Get-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="d77ed-101">Get-AzureRouteTable</span></span>

## <span data-ttu-id="d77ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d77ed-102">SYNOPSIS</span></span>
<span data-ttu-id="d77ed-103">Ottiene una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="d77ed-103">Gets a route table.</span></span>

## <span data-ttu-id="d77ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d77ed-104">SYNTAX</span></span>

```
Get-AzureRouteTable [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d77ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d77ed-105">DESCRIPTION</span></span>
<span data-ttu-id="d77ed-106">Il cmdlet **Get-AzureRouteTable** ottiene una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="d77ed-106">The **Get-AzureRouteTable** cmdlet gets a route table.</span></span>
<span data-ttu-id="d77ed-107">Specificare il parametro *dettagliato* per elencare le route nella tabella di route.</span><span class="sxs-lookup"><span data-stu-id="d77ed-107">Specify the *Detailed* parameter to list the routes in the route table.</span></span>

## <span data-ttu-id="d77ed-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d77ed-108">EXAMPLES</span></span>

### <span data-ttu-id="d77ed-109">Esempio 1: ottenere i dettagli di una tabella di route</span><span class="sxs-lookup"><span data-stu-id="d77ed-109">Example 1: Get details of a route table</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    ApplianceRouteTable           Central US                    Appliance Route Table
```

<span data-ttu-id="d77ed-110">Questo comando consente di ottenere i dettagli di una tabella di route denominata ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="d77ed-110">This command gets the details of a route table named ApplianceRouteTable.</span></span>

## <span data-ttu-id="d77ed-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d77ed-111">PARAMETERS</span></span>

### <span data-ttu-id="d77ed-112">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="d77ed-112">-Detailed</span></span>
<span data-ttu-id="d77ed-113">Indica che questo cmdlet Visualizza le route nella tabella route.</span><span class="sxs-lookup"><span data-stu-id="d77ed-113">Indicates that this cmdlet displays the routes in the route table.</span></span>

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

### <span data-ttu-id="d77ed-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d77ed-114">-Name</span></span>
<span data-ttu-id="d77ed-115">Specifica il nome della tabella di route ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d77ed-115">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77ed-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="d77ed-116">-Profile</span></span>
<span data-ttu-id="d77ed-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d77ed-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d77ed-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d77ed-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d77ed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77ed-119">CommonParameters</span></span>
<span data-ttu-id="d77ed-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d77ed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77ed-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d77ed-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77ed-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d77ed-122">INPUTS</span></span>

## <span data-ttu-id="d77ed-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d77ed-123">OUTPUTS</span></span>

## <span data-ttu-id="d77ed-124">Note</span><span class="sxs-lookup"><span data-stu-id="d77ed-124">NOTES</span></span>

## <span data-ttu-id="d77ed-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d77ed-125">RELATED LINKS</span></span>

[<span data-ttu-id="d77ed-126">New-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="d77ed-126">New-AzureRouteTable</span></span>](./New-AzureRouteTable.md)

[<span data-ttu-id="d77ed-127">Remove-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="d77ed-127">Remove-AzureRouteTable</span></span>](./Remove-AzureRouteTable.md)


